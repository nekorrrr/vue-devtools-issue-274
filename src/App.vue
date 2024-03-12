<script setup lang="ts">
// https://github.com/vueuse/head
// you can use this to manipulate the document head in any components,
// they will be rendered correctly in the html results with vite-ssg
useHead({
  title: 'Vitesse',
  meta: [
    {
      name: 'description',
      content: 'Opinionated Vite Starter Template',
    },
    {
      name: 'theme-color',
      content: () => isDark.value ? '#00aba9' : '#ffffff',
    },
  ],
  link: [
    {
      rel: 'icon',
      type: 'image/svg+xml',
      href: () => preferredDark.value ? '/favicon-dark.svg' : '/favicon.svg',
    },
  ],
})
</script>

<template>
  <n-config-provider h-full>
    <n-notification-provider>
      <n-spin size="large" h-full content-class="h-full" :show="false">
        <n-dialog-provider>
          <RouterView />
        </n-dialog-provider>
      </n-spin>
    </n-notification-provider>
  </n-config-provider>
</template>
