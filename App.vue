<template>
  <div id="app">
    <Add></Add>
    <Info></Info>
    <Footer></Footer>
  </div>
</template>

<script>
import Add from './components/Add';
import Info from './components/Info'
import Footer from './components/Footer'
export default {
  name: 'App',
  components: {
    Add,
    Info,
    Footer,
  },

}
</script>

<style>
#app {
  max-width: 1200px;
  margin: 0 auto;
  padding: 4%;
}
</style>
