<template>
  <div class="show_bar">
    <pre class="html">{{ html }}</pre>
    <div class="result">
      <div class="vertical">
        <avatar username="Top"></avatar>
      </div>
      <avatar username="Left"></avatar>
      <avatar :src="''" :username="username" :size="size" :border-radius="borderRadius" :margin="margin" :initials="initials"></avatar>
      <avatar username="Right"></avatar>
      <div class="vertical">
        <avatar username="Bottom"></avatar>
      </div>
    </div>
  </div>
</template>

<script>
import Avatar from './Avatar'

export default {
  props: {
    username: {
      type: String,
      required: true
    },
    size: {
      type: [String, Number]
    },
    borderRadius: {
      type: String
    },
    margin: {
      type: String
    },
    initials: {
      type: String
    }
  },
  data () {
    return {
      html: `<avatar :src="''"
        :username="username"
        :size="size"
        :border-radius="borderRadius"
        :margin="margin"
        :initials="initials"></avatar>`
    }
  },
  components: {
    Avatar
  }
}
</script>

<style>
  div.show_bar {
    flex: 70%;
    max-width: 70%;
    display: flex;
    flex-direction: column;
    overflow: hidden;
  }
  
  pre.html {
    flex: none;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 20px;
  }
  
  div.result {
    flex: auto;
    background-color: #eee;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    align-content: center;
  }
  
  div.result div.vertical {
    flex: 100%;
    display: flex;
    justify-content: center;
  }
</style>