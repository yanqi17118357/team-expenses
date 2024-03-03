<script setup lang="ts" generic="T extends any, O extends any">


</script>

<template>
  <div>
    <van-nav-bar title="团队成员">
      <template #right>
        <van-icon name="add" size="18" />
      </template>
    </van-nav-bar>
    <van-swipe-cell v-for="obj in 2" :key="obj">
      <van-cell :border="false" title="单元格" value="内容" />
      <template #right>
        <van-button square type="danger" text="删除" />
      </template>
    </van-swipe-cell>
  </div>
</template>
