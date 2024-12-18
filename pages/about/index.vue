<script setup lang="ts">
const handleMessage = () => {
  message.info("This is a normal message");
}
</script>

<template>
  <div class="text-amber-300">aaaaaaaaaaaaaaaaaaaaa</div>
  <a-button @click="handleMessage">
    button
  </a-button>
</template>

<style scoped>

</style>