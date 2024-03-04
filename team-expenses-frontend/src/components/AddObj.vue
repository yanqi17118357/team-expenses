<script setup lang="ts" generic="T extends any, O extends any">
const showProp = defineProps({
  show: Boolean
})
const localShow = ref(showProp.show)
const showModel = computed({
  get: () => showProp.show,
  set: (val) => {
    // handle the mutation here if needed
    localShow.value = val;
  }
})
</script>

<template>
  <van-popup
    v-model:show="showModel"
    position="right"
    props="show"
    :style="{ width: '30%', height: '100%' }"
  />
</template>
