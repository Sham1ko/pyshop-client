<template>
  <q-page class="column items-center justify-center">
    <h4 class="q-ma-none">Hello , {{ user.email }}</h4>
    <br />
    <span
      >Go to
      <router-link to="/profile" style="color: blue; text-decoration: underline"
        >Profile</router-link
      ></span
    >
  </q-page>
</template>

<script setup lang="ts">
import { storeToRefs } from 'pinia';
import { useAuthStore } from 'src/stores/authStore';

const authStore = useAuthStore();

const { user } = storeToRefs(authStore);
</script>
