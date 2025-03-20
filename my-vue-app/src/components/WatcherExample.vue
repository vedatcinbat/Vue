<template>
    <div>
        <input v-model="searchTerm" placeholder="Search...">
        <p>Searching for: "{{ searchTerm }}"</p>
        <button @click="resetSearch">Reset</button>
    </div>
</template>

<script lang="ts" setup>
import { ref, watch } from 'vue'

const searchTerm = ref<string>('')

const resetSearch = (): void => {
    searchTerm.value = ''
}

watch(searchTerm, (newVal: string, oldVal: string) => {
    console.log(`Search term changed from "${oldVal}" to "${newVal}"`)
})
</script>

<style scoped>
/* Optional component styles here */
</style>