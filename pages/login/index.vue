<script setup lang="ts">
import {definePageMeta} from "#imports";
import LoginComponent from "~/components/Login/index.vue";

definePageMeta(
    {
      title: 'Login page',
      name: "LoginPage",
      layout: 'empty',
    }
)
</script>

<template>
  <div>
    <LoginComponent/>
  </div>
</template>

<style scoped>

</style>