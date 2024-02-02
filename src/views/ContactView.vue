<script setup lang="ts">
import { ref } from 'vue';

     const state = ref({
        id: "title1",
        name: "",
        isLoading:false,
     });

    const handleClick = () => {
        state.value.isLoading = !state.value.isLoading
        console.log(state.value.name);
    }
      

</script>


<template>
    <h1 :id="state.id" >Hello! Welcome</h1>
    <input type="text" name="name" v-model="state.name">
    <p
    class="para"
    :class="{'para2': state.isLoading}"
    > {{ state.name }} </p>
    <button @click="handleClick">Click</button>
</template>

<style>

#title1
{
    color: violet;
}

.para{
    color: blueviolet;
}

.para2{
    color: red;
}

input {
    height: 30px;
}

button{
    margin-top: 15px;
}

</style>