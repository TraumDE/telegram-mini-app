<script setup lang="ts">
import {
  usePopup,
  useMiniApp,
  FullscreenViewport,
  ExpandedViewport,
  MainButton,
  SecondaryButton,
  useQrScanner,
} from 'vue-tg'

const miniApp = useMiniApp()
const popup = usePopup()
const qrScanner = useQrScanner()

const handleMainButtonClick = (): void => {
  if (popup.isVersionAtLeast('6.2')) popup.showAlert('Приложение сейчас закроется', miniApp.close)
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
  <main-button @click="handleMainButtonClick" text="Закрыть приложение" />
  <secondary-button @click="handleSecondaryButtonClick" text="Открыть QR-Сканер" />
</template>

<style scoped>
* {
  color: white;
}
</style>
