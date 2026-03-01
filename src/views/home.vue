<template>
    <h1>主页</h1>
    <ul>
        <li class="sp" v-for="pj in pjList" :key="pj.id">{{ pj.name }}</li>
    </ul>
</template>

<script setup>
    import { reactive } from 'vue';
    let pjList = reactive([
        { id: '001', name: '1', price: 1, src: ''},
        { id: '002', name: '2', price: 2, src: ''},
        { id: '003', name: '3', price: 3, src: ''},
        { id: '004', name: '4', price: 4, src: ''},
        { id: '005', name: '5', price: 5, src: ''}
    ])
</script>

<style scoped>
    h1{
        text-align: center;
        font-size: 30px;
    }
    ul{
        list-style: none;
        padding: 0;
        margin: 0 auto;
        width: 90%;
        display: flex;
        flex-wrap: wrap;
        justify-content: flex-start;
    }
    .sp{
        display: inline-block;
        width: 400px;
        height: 400px;
        border: 1px solid #000;
        margin: 10px;
    }
</style>