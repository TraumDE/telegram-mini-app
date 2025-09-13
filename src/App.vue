<script setup lang="ts">
import { Alert } from 'vue-tg'
import { FullscreenViewport } from 'vue-tg'
import { ExpandedViewport } from 'vue-tg'
import { MainButton } from 'vue-tg'
import { SecondaryButton } from 'vue-tg'
</script>

<template>
  <fullscreen-viewport />
  <expanded-viewport />
  <h1>You did it!</h1>
  <p>
    Visit <a href="https://vuejs.org/" target="_blank" rel="noopener">vuejs.org</a> to read the
    documentation
  </p>
  <main-button text="Main button" />
  <secondary-button text="Secondary button" />
  <alert message="Hello!" />
</template>

<style scoped>
* {
  color: white;
}
</style>
