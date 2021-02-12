<template lang="pug">
  #app
    h1 {{ msg }}
    p {{ 1 * 2}}
    p {{ 'Hola' + 'Mundo' }}
    p {{ person.name }}
    p {{ person.name.toUpperCase() }}
    p {{ JSON.stringify(person) }}
    p {{ true ? 'true' : 'false' }}
</template>

<script>

export default {
  name: 'App',
  data () {
    return {
      msg: 'Hola Vue',

      person: {
        name: 'Eric'
      }
    }
  }
}
</script>

<style lang="scss">
  @import './scss/main.scss'
</style>
