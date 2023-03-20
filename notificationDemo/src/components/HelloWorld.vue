<script setup lang="ts">
import { ref } from 'vue'

import { NButton, useNotification } from 'naive-ui'
defineProps<{ msg: string }>()
const count = ref(0)
const notification = useNotification()

const onButton = () => {
  const message = {
    "statusCode": 400,
    "data": null,
    "succeeded": false,
    "errors": "有数据没有处理完毕, 请在日志中查看! ,\r\n 日志路径: D:\\Code\\C#\\General\\General\\General.Web.Entry\\bin\\Debug\\net7.0\\log\\AgencyNameDots.txt",
    "extras": null,
    "timestamp": 1679293131
  }
  notification.warning({
    title: '警告',
    description: message.errors
  })
}
</script>

<template>
  <n-button @click="onButton">Click Me</n-button>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
