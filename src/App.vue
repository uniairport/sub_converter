<script setup lang="ts">
import ParamsSets from './components/ParamsSets/ParamsSet.vue';
import { useParamsStore } from './stores/paramsStore';
import Swal from 'sweetalert2';
import { onMounted } from 'vue';

const store = useParamsStore()

window.addEventListener('beforeunload', () => {
    store.saveData()
})

onMounted(async () => {
    await Swal.fire({
        icon: 'info',
        title: 'Uni Network',
        text: `Uni，致力于打造一个精品机场，独有隧道技术在保障系节点稳定的同时又能让保证三网用户在速度方面的体验，全节点流媒体解锁保证，有机场专属emby，含奈非、迪士尼资源 
官网： fanmagic.top`
    })
})
</script>

<template>
    <header>
        <v-card title="Subscription Converter" color="primary" class="params header">
        </v-card>
    </header>
    <ParamsSets></ParamsSets>
    <footer id="footer">
        2022 - present by <a href="https:/www.chinq.xyz">CQBerry</a>
    </footer>
</template>

<style scoped>
#footer {
    text-align: center;
}

#footer>a {
    text-decoration-line: none;
    color: black;
}
</style>