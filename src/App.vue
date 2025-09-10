<script setup>
  import LoginForm from '@/components/LoginForm.vue'
  import SearchFilm from '@/components/SearchFilm.vue'
  import { ref } from 'vue'

  const loggedIn = ref(true)
</script>

<template>
  <LoginForm v-if="loggedIn === false"/>
  <SearchFilm v-else/>
</template>

<style>
  @import './assets/base.css';
</style>
