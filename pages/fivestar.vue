<template>
  <div id="app">
    <WebViewer :path="`/webviewer`" url="/pdfs/football_package.pdf"/>
  </div>
</template>

<script>
import WebViewer from '../components/WebViewer.vue'
export default {
  name: 'app',
  components: {
    WebViewer
  },
  data () {
    return {
       
    }
  }
}
</script>

<style>
html,
body {
  margin: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0 auto;
  height: 100vh;
}
#webviewer{
  height: 100vh;
}
</style>