<template>
    <div>
        <h1>{{ title }}</h1>
        <input v-model="userInput" placeholder="Type something...">
        <p>You typed: {{ userInput }}</p>
        <button @click="updateTitle">Update Title</button>
    </div>
</template>

<script lang="ts" setup>
import { ref } from 'vue'

const title = ref<string>('Hello Vue with TypeScript')
const userInput = ref<string>('')

function updateTitle(): void {
    title.value = userInput.value
}

</script>

<style scoped>
/* Optional component styles here */
</style>