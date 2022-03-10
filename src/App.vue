<template>
  <div id="app">
    <MainHeader />
    <MainContent />
  </div>
</template>

<script>

import MainHeader from './components/Header.vue'
import MainContent from './components/Main.vue'

export default {
  name: 'App',
  components: {
    MainHeader,
    MainContent
}
}
</script>

<style lang="scss">

@import './assets/scss/common.scss';
@import './assets/scss/mixin.scss';

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

img {
  max-width: 100%;
}

ul {
  list-style: none;
}

.container {
  @include container
}

#app {
  font-family: "Montserrat", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  height: 100vh;
  display: flex;
  flex-direction: column;
}

</style>
