<script setup>
import { ref } from 'vue'
import sonComVue from '@/components/son-com.vue'
const money = ref(100)
const changeMoney = () => {
  money.value += 100
}
const payMoney = (num) => {
  money.value -= num
}
</script>
<template>
  <h3>
    父组件 - {{ money }}
    <button @click="changeMoney">挣钱</button>
    <sonComVue :money="money" @changeMoney="payMoney"></sonComVue>
  </h3>
</template>