<script setup>
const props = defineProps({
  money: Number
})
const emit = defineEmits(['changeMoney'])
const payMoney = () => {
  emit('changeMoney', 10)
}
</script>

<template>
  <div class="son">
    <h3>子组件 - {{ money }}</h3>
    <button @click="payMoney">花钱</button>
  </div>
</template>

<style scoped>
.son {
  border: 1px solid #000;
  padding: 20px;
}
</style>