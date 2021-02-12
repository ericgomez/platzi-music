<template lang="pug">
  #app
    input(v-model="name")

    button(v-on:click="format") Format
    button(@click="format") Format

    p {{ formattedName }}
</template>

<script>

export default {
  name: 'App',
  data () {
    return {
      name: '',
      formattedName: ''
    }
  },

  methods: {
    format () {
      this.formattedName = this.name.split(' ').join('-').toUpperCase()
    }
  }
}
</script>

<style lang="scss">
  @import './scss/main.scss'
</style>
