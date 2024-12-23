<script setup lang="ts">
defineOptions({
  name: "LoginComponent"
})

const userName = ref<string>('')
const password = ref<string>('')
const error = ref<string | null>(null)

const handleSubmit = () => {
  console.log("login")
}

</script>

<template>
  <div class="q-pa-md" style="max-width: 400px">

    <q-form
        @submit="handleSubmit"
        class="q-gutter-md"
    >
      <q-input
          filled
          v-model="userName"
          label="Your name *"
          hint="Name and surname"
          lazy-rules
          :rules="[ val => val && val.length > 0 || 'Please type something']"
      />

      <q-input
          filled
          type="number"
          v-model="password"
          label="Your age *"
          lazy-rules
          :rules="[
          val => val !== null && val !== '' || 'Please type your age',
          val => val > 0 && val < 100 || 'Please type a real age'
        ]"
      />

      <div>
        <q-btn label="Submit" type="submit" color="primary"/>
      </div>
    </q-form>

  </div>
</template>

<style scoped>

</style>