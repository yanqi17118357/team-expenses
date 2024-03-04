<script setup lang="ts" generic="T extends any, O extends any">
const active = ref(0)
const router = useRouter()
function toHome() {
  router.push('/')
}
function toTeam() {
  router.push('/team')
}
</script>

<template>
  <div>
    <nav mt-6 inline-flex gap-2 text-xl>
      <van-tabbar v-model="active">
        <van-tabbar-item icon="home-o" @click="toHome">
          主页
        </van-tabbar-item>
        <van-tabbar-item icon="friends-o" @click="toTeam">
          团队
        </van-tabbar-item>
      </van-tabbar>
    </nav>
  </div>
</template>

