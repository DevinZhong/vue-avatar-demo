<template>
  <div class="sidebar">
    <div>
      <label for="username">username</label>
      <input id="username" type="text" @keyup="setUsername">
    </div>
    <div>
      <label for="size">size</label>
      <input id="size" type="text" @keyup="setSize">
    </div>
    <div>
      <label for="borderRadius">borderRadius</label>
      <input id="borderRadius" type="text" @keyup="setBorderRadius">
    </div>
    <div>
      <label for="margin">margin</label>
      <input id="margin" type="text" @keyup="setMargin">
    </div>
    <div>
      <label for="initials">initials</label>
      <input id="initials" type="text" @keyup="setInitials">
    </div>
  </div>
</template>

<script>
export default {
  props: {
    setUsername: {
      type: Function,
      required: true
    },
    setSize: {
      type: Function,
      required: true
    },
    setBorderRadius: {
      type: Function,
      required: true
    },
    setMargin: {
      type: Function,
      required: true
    },
    setInitials: {
      type: Function,
      required: true
    }
  }
}
</script>

<style>
  div.sidebar {
    flex: 30%;
    background-color: #eee;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  div.sidebar > div {
    margin: 1rem;
    display: flex;
    flex-direction: column;
    font-size: 2rem;
  }
  div.sidebar input {
    font-size: 1.5rem;
  }
</style>