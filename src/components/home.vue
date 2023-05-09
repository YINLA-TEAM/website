<template>

<div v-if="view === 1">
    <button @click="changeView(2)">進入</button>

        
</div>

<div v-if="view === 2">
    <button @click="changeView(3)">簡介</button>
    <button @click="changeView(4)">社群</button>
    <button @click="changeView(1)">返回</button>
</div>

<div v-if="view === 3">
    <p>balabala</p>
    <button @click="changeView(2)">返回</button>
</div>

<div v-if="view === 4">
    <button onclick="location.href='https://discord.gg/mnCHdBbh65'">Discord</button>
    <button onclick="location.href='https://github.com/YINLA-TEAM'">GitHub</button>
    <button>other</button>
    <br> <br>
    <button @click="changeView(2)">返回</button>
</div>

</template>

<script setup>
import { ref } from 'vue'
const view = ref(1)
    const changeView = (index) => {
        view.value = index
    }
</script>

<style scoped>
</style>
