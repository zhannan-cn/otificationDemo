<script setup lang="ts">
import { NButton, useNotification, NNotificationProvider, NConfigProvider } from 'naive-ui'
import HelloWorld from './components/HelloWorld.vue';


// const onButton = () => {
//   notification.info({
//     title: 'Info',
//     content: 'This is a info message.'
//   })
// }

</script>

<template>
  <n-config-provider>
    <n-notification-provider>
      <HelloWorld msg="Welcome to Your Vue.js + TypeScript App" />
    </n-notification-provider>
  </n-config-provider>
</template>

<style scoped>
</style>
