<template>
    <img id="yinla_logo" src="/106425898.png" alt="YINLA_LOGO">
    <h1 class="team_name" style="moveUp">YINLA</h1>
    <div v-if="view === 1">
        
        <button @click="changeView(2)">進入</button>
    </div>

    <div v-if="view === 2">
        
        <button @click="changeView(3)">簡介</button>
        <button @click="changeView(4)">社群</button>
        <button @click="changeView(1)">返回</button>
    </div>

    <div v-if="view === 3">
        <h3 class="info">創立於 2022年<br>創辦人 <a  href="https://github.com/YinCheng0106" target="_blank">YinCheng</a></h3>
        <button @click="changeView(2)">返回</button>
    </div>

    <div v-if="view === 4">
        <br>
        <button onclick="location.href='https://discord.gg/mnCHdBbh65'">
            Discord
        </button>
        <button onclick="location.href='https://github.com/YINLA-TEAM'">
            GitHub
        </button>
        <button>other</button>
        <br/>
        <br/>
        <button @click="changeView(2)">返回</button>
    </div>
</template>

<script setup>
import { reactive, ref, watch } from "vue";
const view = ref(1);
const changeView = (index) => {
    view.value = index;
};
const moveUp = reactive({
    fonSize : '60px',
    animation : 'openIn 1s ease-in-out',
    transform: 'translateY(0)'
})

watch(view.value, () => {
    if(view.value === 2 || 3 || 4){
        moveUp.transform = 'translateY(20px)'
    }
})
</script>

<style scoped>
#yinla_logo {
    border-radius: 45px;
    animation: openIn 1.5s ease-in-out;
}

h1 {
    position: static;
    font-size: 60px;
}

button, .info, h1 {
    animation: openIn 1.5s ease-in-out;
}


@keyframes openIn{
        0% {
            opacity: 0;
        }
        100% {
            opacity: 1;
        }
    }


</style>
