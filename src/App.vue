<template lang="pug">
  #app
    input(v-model="name")
    p {{ name }}

    a(v-bind:href="url") Link
    a(:href="url") Link
</template>

<script>

export default {
  name: 'App',
  data () {
    return {
      name: '',

      url: 'https://platzi.com'
    }
  }
}
</script>

<style lang="scss">
  @import './scss/main.scss'
</style>
