<template>
  <md-whiteframe md-elevation="0">
    <md-layout md-gutter>
      <md-layout>
        Магазин
      </md-layout>
      <md-layout>
        <div class="logo"></div>
      </md-layout>
      <md-layout>
        Услуги
      </md-layout>
    </md-layout>
  </md-whiteframe>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<style lang="scss">
  .logo {
    width: 200px;
    height: 200px;
    background: url('./assets/logo.svg')
  }
</style>
