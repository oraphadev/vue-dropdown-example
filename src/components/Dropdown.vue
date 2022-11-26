<template>
  <div :class="['dropdown', { open }]">
    <button
      tabindex="0"
      @focusout="close"
      @click="toggle"
    >
      <span>tune</span>
      Filtrar vagas
      <span id="icon">{{ icon }}</span>
    </button>
    <ul>
      <li>
        <span>dns</span>
        Backend
      </li>
      <li>
        <span>palette</span>
        Frontend
      </li>
      <li>
        <span>bolt</span>
        Fullstack
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'TheDropdown',
  data: () => ({
    open: false,
  }),
  computed: {
    icon() {
      return !this.open ? 'expand_more' : 'close'
    }
  },
  methods: {
    close() {
      this.open = false
    },
    toggle() {
      this.open = !this.open
    },
  },
}
</script>

<style scoped>
.dropdown,
button {
  position: relative;
}

.dropdown.open button {
  background: #15a480;
}

.dropdown button {
  z-index: 2;
}

.dropdown button #icon {
  margin-left: auto;
}

button,
li {
  display: flex;
  align-items: center;
  gap: 10px;
  padding: 0 16px;
  width: 240px;
  height: 64px;
  border-radius: 6px;
  color: #f9f9f9;
  background: #252525;
  border: 0;
  cursor: pointer;
  transition: 0.3s;
  font-size: 16px;
}

button:hover{
  background: #3a3a3a;
}

ul {
  list-style: none;
  padding: 0;
  margin: 0;
  position: absolute;
  overflow: hidden;
  z-index: 1;
  top: 61px;
  width: 100%;
  opacity: 0;
  visibility: hidden;
  border-bottom-left-radius: 6px;
  border-bottom-right-radius: 6px;
  background: #3e3e3e;
  translate: 0 -16px;
  transition: 0.3s;
}

li {
  width: 100%;
  height: 56px;
  border-radius: 0;
}

li:hover {
  background: #383838;
}

.dropdown.open ul {
  opacity: 1;
  translate: 0;
  visibility: visible;
}
</style>
