<script setup lang="ts">
import { ref } from 'vue';

const emits = defineEmits(['add'])
const name = ref('')

function onAdd(){
    emits('add', 'name.value')
    name.value = ''
}

function changeText(e: Event){
    name.value = (e.target as HTMLInputElement).value
}
</script>

<template>
    <div>
        <input v-model="name" type="text" name="" id="">
        <button @click="onAdd">Add</button>
    </div>
</template>