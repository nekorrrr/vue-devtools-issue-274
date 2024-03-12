<template>
  <main
    px-48 py-4
    text="center gray-700 dark:gray-200"
  >
    <n-space
      vertical size="large"
      class="!border-3"
      rounded-xl border-inherit border-solid p-4 text-left shadow-md
    >
      <n-layout>
        <n-layout-content>
          <RouterView />
        </n-layout-content>
      </n-layout>
    </n-space>
  </main>
</template>
