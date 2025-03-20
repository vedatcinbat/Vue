<template>
    <div>
        <p>Open your console to see lifecycle hook messages</p>
        <button @click="updateContent">Update Content</button>
        <p>{{ content }}</p>
    </div>
</template>

<script lang="ts" setup>
import { ref, onBeforeMount, onMounted, onBeforeUpdate, onUpdated, onBeforeUnmount, onUnmounted } from 'vue'

const content = ref<string>('Initial content')

onMounted(() => {
    console.log('Component has been mounted')
})

onUpdated(() => {
    console.log('Component has been updated')
})

onUnmounted(() => {
    console.log('Component has been unmounted')
})

function updateContent(): void {
    content.value = 'Content Updated at ' + new Date().toLocaleTimeString()
}
</script>

<style scoped>
/* Optional component styles here */
</style>