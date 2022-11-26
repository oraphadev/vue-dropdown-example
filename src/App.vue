<template>
  <div id="app">
    <Dropdown />
  </div>
</template>

<script>
import Dropdown from '@/components/Dropdown'

export default {
  name: 'App',
  components: {
    Dropdown
  }
}
</script>

<style>
* {
  box-sizing: border-box;
  font-family: 'Outfit';
}

body, html {
  margin: 0;
  padding: 0;
  background: #121214;
}

span {
  font-family: 'Material Symbols Outlined';
  font-weight: normal;
  font-style: normal;
  font-size: 24px;
  line-height: 1;
  letter-spacing: normal;
  text-transform: none;
  display: inline-block;
  white-space: nowrap;
  word-wrap: normal;
  direction: ltr;
  font-feature-settings: 'liga';
  -webkit-font-feature-settings: 'liga';
  -webkit-font-smoothing: antialiased;
}
</style>

<style scoped>
#app {
  align-items: center;
  display: flex;
  justify-content: center;
  width: 100%;
  min-height: 100vh;
}
</style>
