<template>
<md-layout class="main">
  <md-whiteframe md-tag="md-toolbar" :md-elevation="elevation" class="app md-transparent" 
  :class="elevation ? 'md-dense' : 'md-large'">
    <div class="md-toolbar-container">
      <md-button class="md-icon-button" @click="$refs.sidenav.toggle()">
        <md-icon>menu</md-icon>
      </md-button>

      <span style="flex: 1"></span>

      <md-button class="md-icon-button">
        <md-icon>search</md-icon>
      </md-button>

      <md-button class="md-icon-button">
        <md-icon>view_module</md-icon>
      </md-button>
    </div>
  </md-whiteframe>
  <md-layout class="content"></md-layout>
</md-layout>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      elevation: 0
    }
  },
  mounted() {
    const self = this;
    document.addEventListener('scroll', () => {
      self.elevation = window.pageYOffset ? 5 : 0;
    })
  }
}
</script>

<style lang="scss">
  body {
    display: flex;
  }
  .app {
    max-height: 300px;
    position: fixed;
    left: 0;
    right: 0;
    top: 0;
  }
  .content {
    background: url('./assets/back.jpg') center no-repeat;
  }
  .logo {
    width: 200px;
    height: 200px;
    background: url('./assets/logo.svg')
  }
</style>
