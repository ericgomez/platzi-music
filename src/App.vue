<template lang="pug">
  #app

    pm-header

    pm-notification(v-show="showNotification")
      p(slot="body") No se encontraron resultados

    pm-loader(v-show="isLoading")

    section.section(v-show="!isLoading")
      nav.nav
        .container
          input.input.is-large(type="text", placeholder="Buscar canciones", v-model="searchQuery")
          a.button.is-info.is-large(@click="search") Buscar
          a.button.is-danger.is-large &times;

      .container
        p
          small {{ searchMessage }}

      .container.results
        .columns.is-multiline
          .column.is-one-quarter(v-for="t in tracks")
            PmTrack(:class="{ 'is-active' : t.id === selectedTrack }", :track="t", @select="setSelectedTrack")

    pm-footer

</template>

<script>
import trackService from '@/services/track'
import PmHeader from '@/components/layout/Header'
import PmFooter from '@/components/layout/Footer'

import PmTrack from '@/components/Track'
import PmLoader from '@/components/shared/Loader'

import PmNotification from '@/components/shared/Notification'

export default {
  name: 'App',
  components: { PmHeader, PmFooter, PmTrack, PmLoader, PmNotification },
  data () {
    return {
      searchQuery: '',
      tracks: [],

      isLoading: false,
      showNotification: false,

      selectedTrack: ''
    }
  },

  computed: {
    searchMessage () {
      return `Encontrados: ${this.tracks.length}`
    }
  },

  watch: {
    showNotification () {
      if (this.showNotification) {
        setTimeout(() => {
          this.showNotification = false
        }, 3000)
      }
    }
  },

  methods: {
    search () {
      if (!this.searchQuery) { return } // Validamos si intentan buscar con el campo vacío

      this.isLoading = true

      trackService.search(this.searchQuery)
        .then(res => {
          this.showNotification = res.tracks.total === 0 // Validamos tracks.total desde la api
          this.tracks = res.tracks.items
          this.isLoading = false
        })
    },
    setSelectedTrack (id) {
      this.selectedTrack = id
    }
  }
}
</script>

<style lang="scss">
  @import './scss/main.scss';

  .results {
    margin-top: 50px;
  }

  .is-active {
    border: 3px #23d160 solid;
  }

</style>
