<script setup lang="ts" generic="T extends any, O extends any">
const objList = ref([
  {
    id: 1,
    num: 1,
    name: '张三',
    isPaid: true,
  },
  {
    id: 2,
    num: 1,
    name: '李四',
    isPaid: true,
  },
  {
    id: 3,
    num: 1,
    name: '王五',
    isPaid: false,
  },
])

</script>

<template>
  <div>
    <AddObj :show="false"/>
    <van-nav-bar title="物品清单">
      <template #right>
        <van-icon name="add" size="18" @click="show = true" />
      </template>
    </van-nav-bar>
    <van-card
      v-for="obj in objList" :key="obj.id" :num="obj.num" price="2.00" desc="描述信息" :title="obj.name"
      thumb="https://fastly.jsdelivr.net/npm/@vant/assets/ipad.jpeg" origin-price="10.00"
    >
      <template #tags>
        <van-tag plain :type="obj.isPaid ? 'success' : 'danger'">
          {{ obj.isPaid ? '已付清' : '未付清' }}
        </van-tag>
      </template>
    </van-card>
  </div>
</template>
