
<template>
    <p>父组件当前的值为：{{ number }}</p>
    <CustomSubComponent @updateCount = "updateCount" />
</template>

<script setup>
import { ref } from 'vue';
import CustomSubComponent from './CustomSubComponent.vue';
const number = ref(10);
const updateCount = (value) => {
    number.value += value;
}
</script>