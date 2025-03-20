<template>
    <div>
        <p>Original: {{  message }}</p>
        <p>Reserved: {{ reversedMessage }}</p>
        <button @click="changeMessage">Change Message</button>
    </div>
</template>

<script lang="ts" setup>
    import { ref, computed } from 'vue'

    const message = ref<string>('Hello Vue with TypeScript')
    const reversedMessage = computed<string>(() => {
        return message.value.split('').reverse().join('')
    })

    function changeMessage(): void {
        message.value = 'Vue 3 + TypeScript is awesome!'
    }
</script>

<style scoped>
    /* Optional component styles here */
</style>