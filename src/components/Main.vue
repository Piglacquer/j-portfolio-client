<template>
    <div id='main'>
        <Header :scrolled='scrolled' :headerVisible='headerVisible' :yScroll='yScroll' v-on:showHeader='toggleHeader'/>
        <h1> YOOOOOO </h1>
        <router-view />
        <Footer />
    </div>
</template>

<script>
import Header from './Header'
import Footer from './Footer'

export default {
    name: 'Main',
    components: {
        Header,
        Footer
    },
    data () {
        return {
            scrolled: false,
            yScroll: 0,
            previousHighYScroll: 0,
            previousLowYScroll: 0,
            headerVisible: false 
        }
    },
  methods: {
    handleScroll() {
        console.log('HAY')
        this.yScroll = window.scrollY
        if (this.yScroll < this.previousHighYScroll || this.yScroll < this.previousLowYScroll) {
          this.previousLowYScroll = this.yScroll
          this.previousHighYScroll = this.yScroll + 1
          this.scrolled = false
        }
        else {
          this.previousHighYScroll = this.yScroll
          this.scrolled = true
        }
      },
      toggleHeader() {
        this.headerVisible = !this.headerVisible
        this.scrolled = false
      }
    },
    beforeMount() {
        console.log('BEFORE MOUNT')
        window.addEventListener('scroll', this.handleScroll)
    },
    beforeDestroy() {
        console.log('DESTROY')
        window.removeEventListener('scroll', this.handleScroll)
    }
}
</script>

<style scoped>
 #main{
     display: flex;
     flex-flow: column nowrap;
     justify-content: space-between;
     height: 120vh;
 } 
 h1{
     font-size: 5rem;
 }
</style>
