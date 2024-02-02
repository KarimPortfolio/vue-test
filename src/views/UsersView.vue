<script lang="ts" setup>
import { reactive } from 'vue';


    const state = reactive({
        users:[]
    })
</script>

<template>
    <h1>All our users</h1>
    <div class="div">
        <div v-for="user in state.users">
            
        </div>
    </div>
</template>

<style>
.div{
    margin-top: 30px;
    padding: 20px;
}
</style>

