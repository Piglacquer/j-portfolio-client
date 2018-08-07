<template>
  <div id="app">
    <div>
      <Header/>
      <router-view/>
      <Footer/>
    </div>
  </div>
</template>

<script>
import Header from './components/Header'
import Footer from './components/Footer'

export default {
  name: 'App',
  components: {
    Header,
    Footer
  }
}
</script>

<style>
  #app {
    background-color: white;
  }
</style>
