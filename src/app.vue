<template>
  <div class="main">
    <input type="text" v-model="text" />
    <div class="hello">Hello {{ text }}!</div>
  </div>

  <div id="editor">
    <textarea v-model="input" debounce="300"></textarea>
    <div v-html="input | marked"></div>
  </div>
</template>

<script>
  export default {
    replace: false,
    el: '#editor',
  	data() {
      return {
        text: 'Vuejs',
        input: '# hello'
      }
    }
  }
</script>
