<template>
  <div id="app">
    <navi />
    <boxtarge />
  </div>
</template>

<script>
import navi from './components/navi.vue'
import boxtarge from './components/boxtarge.vue'

export default {
  name: 'app',
  components: {
    navi,
    boxtarge
  }
}
</script>

<style>
*{
    box-sizing: border-box;
    padding: 0px;
    margin: 0px;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  text-align: center;
    background-color:#eceff1; 
  color: #2c3e50;
}

</style>
