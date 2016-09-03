<template>
  <div id="app">
    <sidebar :set-username="setUsername" :set-size="setSize" :set-border-radius="setBorderRadius" :set-margin="setMargin" :set-initials="setInitials"></sidebar>
    <show-bar :username="username" :size="size" :border-radius="borderRadius" :margin="margin" :initials="initials"></show-bar>
  </div>
</template>

<script>
import Sidebar from './components/Sidebar'
import ShowBar from './components/ShowBar'

export default {
  data () {
    return {
      username: 'Avatar',
      size: '50',
      borderRadius: '',
      margin: '',
      initials: ''
    }
  },
  components: {
    Sidebar,
    ShowBar
  },
  methods: {
    setUsername (e) {
      this.username = e.target.value
    },
    setSize (e) {
      this.size = e.target.value
    },
    setBorderRadius (e) {
      this.borderRadius = e.target.value
    },
    setMargin (e) {
      this.margin = e.target.value
    },
    setInitials (e) {
      this.initials = e.target.value
    }
  }
}
</script>

<style>
  html {
    height: 100%;
  }
  
  body {
    margin: 0;
    padding: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100%;
  }
  
  #app {
    width: 100vw;
    height: 100vh;
    flex: auto;
    align-self: stretch;
    display: flex;
  }
</style>