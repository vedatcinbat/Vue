<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import DataBindingExample from './components/DataBindingExample.vue'
import ComputedExample from './components/ComputedExample.vue'
import WatcherExample from './components/WatcherExample.vue'
import LifecycleHooksExample from './components/LifecycleHooksExample.vue'
</script>

<template>
  <DataBindingExample />
  <ComputedExample />
  <WatcherExample />
  <LifecycleHooksExample />
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}

.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}

.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
