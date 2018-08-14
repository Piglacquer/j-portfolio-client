<template>
  <div id="app">
    <div id="wrapper">
      <router-view/>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  components: {
  }
  // data () {
  // return {
  //   scrolled: false,
  //   yScroll: 0,
  //   previousHighYScroll: 0,
  //   previousLowYScroll: 0,
  //   headerVisible: false 
  //   }
  // },
  // methods: {
  //   handleScroll () {
  //       this.yScroll = window.scrollY
  //       if (this.yScroll < this.previousHighYScroll || this.yScroll < this.previousLowYScroll) {
  //         this.previousLowYScroll = this.yScroll
  //         this.previousHighYScroll = this.yScroll + 1
  //         this.scrolled = false
  //       }
  //       else {
  //         this.previousHighYScroll = this.yScroll
  //         this.scrolled = true
  //       }
  //     },
  //     toggleHeader() {
  //       this.headerVisible = !this.headerVisible
  //       this.scrolled = false
  //     }
  //   },
  //   beforeMount () {
  //         window.addEventListener('scroll', this.handleScroll)
  //     },
  //   beforeDestroy () {
  //         window.removeEventListener('scroll', this.handleScroll)
  //   }
}
</script>

<style>
  #app {
    background-color: white;
  }

  #wrapper {
    display: flex;
    flex-flow: column nowrap;
    justify-content: space-between;
    height: 100vh;
    width: 100vw;
  }

  /* Header {
    position: absolute;
    color: yellow;
  } */
  /* RESET CSS */
  html, body, div, span, applet, object, iframe,
  h1, h2, h3, h4, h5, h6, p, blockquote, pre,
  a, abbr, acronym, address, big, cite, code,
  del, dfn, em, img, ins, kbd, q, s, samp,
  small, strike, strong, sub, sup, tt, var,
  b, u, i, center,
  dl, dt, dd, ol, ul, li,
  fieldset, form, label, legend,
  table, caption, tbody, tfoot, thead, tr, th, td,
  article, aside, canvas, details, embed, 
  figure, figcaption, footer, header, hgroup, 
  menu, nav, output, ruby, section, summary,
  time, mark, audio, video {
    margin: 0;
    padding: 0;
    border: 0;
    font-size: 100%;
    font: inherit;
    vertical-align: baseline;
  }
  /* HTML5 display-role reset for older browsers */
  article, aside, details, figcaption, figure, 
  footer, header, hgroup, menu, nav, section {
    display: block;
  }
  body {
    line-height: 1;
  }
  ol, ul {
    list-style: none;
  }
  blockquote, q {
    quotes: none;
  }
  blockquote:before, blockquote:after,
  q:before, q:after {
    content: '';
    content: none;
  }
  table {
    border-collapse: collapse;
    border-spacing: 0;
  }
</style>
