<script setup lang="ts">
import { usePopup } from 'vue-tg'
import { Alert } from 'vue-tg'
import { FullscreenViewport } from 'vue-tg'
import { ExpandedViewport } from 'vue-tg'
import { MainButton } from 'vue-tg'
import { SecondaryButton } from 'vue-tg'

const popup = usePopup()

const handleMainButtonClick = (): void => {
  if (popup.isVersionAtLeast('6.2')) popup.showAlert('Привет')
  return
}
</script>

<template>
  <fullscreen-viewport />
  <expanded-viewport />
  <h1>You did it!</h1>
  <p>
    Visit <a href="https://vuejs.org/" target="_blank" rel="noopener">vuejs.org</a> to read the
    documentation
  </p>
  <main-button @click="handleMainButtonClick" text="Main button" />
  <secondary-button text="Secondary button" />
</template>

<style scoped>
* {
  color: white;
}
</style>
