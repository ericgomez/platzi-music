<template lang="pug">
  #app
    pm-header

    router-view

    pm-footer

</template>

<script>
import PmHeader from '@/components/layout/Header'
import PmFooter from '@/components/layout/Footer'

export default {
  name: 'App',
  components: { PmHeader, PmFooter }
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
