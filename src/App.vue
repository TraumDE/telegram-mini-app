<script setup lang="ts">
import { Alert } from 'vue-tg'
import { FullscreenViewport } from 'vue-tg'
</script>

<template>
  <FullscreenViewport />
  <h1>You did it!</h1>
  <p>
    Visit <a href="https://vuejs.org/" target="_blank" rel="noopener">vuejs.org</a> to read the
    documentation
  </p>
  <alert message="Hello!" />
</template>

<style scoped>
* {
  color: white;
}
</style>
