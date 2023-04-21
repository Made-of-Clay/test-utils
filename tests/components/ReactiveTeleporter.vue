<template>
  <button @click="count++">
    Increment
  </button>

  <span id="outerCount" v-text="count" />

  <Teleport to="body">
    <span id="innerCount" v-text="count" />
  </Teleport>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const count = ref(0)
</script>
