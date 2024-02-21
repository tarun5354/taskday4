<template>
    <h3>handling the events</h3>
    <div>
        <button v-on:click="count++"> counter</button>
        <div>counter: {{ count }}</div>
    </div>
</template>


<script setup>
import { ref } from 'vue';


const count=ref(0);

</script>