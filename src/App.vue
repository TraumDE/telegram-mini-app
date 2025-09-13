<script setup lang="ts">
import {
  FullscreenViewport,
  ExpandedViewport,
  MainButton,
  SecondaryButton,
  useQrScanner,
  useHomeScreen,
} from 'vue-tg'

const qrScanner = useQrScanner()
const homeScreen = useHomeScreen()

const handleMainButtonClick = (): void => {
  if (homeScreen.isVersionAtLeast('8.0')) homeScreen.addShortcut()
  return
}

const handleSecondaryButtonClick = (): void => {
  if (qrScanner.isVersionAtLeast('6.4')) qrScanner.show({ text: 'Отсканируйте QR' })
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
  <main-button @click="handleMainButtonClick" text="Добавит окно" />
  <secondary-button @click="handleSecondaryButtonClick" text="Открыть QR-Сканер" />
</template>

<style scoped>
* {
  color: white;
}
</style>
