<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
  export default {
    name: 'app',
    mounted() {
      const { NODE_ENV } = process.env;
    document.documentElement.className = NODE_ENV;
    }
  }
</script>