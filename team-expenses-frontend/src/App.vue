<script setup lang="ts" generic="T extends any, O extends any">

</script>

<template>
  <main font-sans text="gray-700 dark:gray-200">
    <van-config-provider :theme="isDark ? 'dark' : 'light'">
      <RouterView />
      <TheFooter />
    </van-config-provider>
  </main>
</template>
