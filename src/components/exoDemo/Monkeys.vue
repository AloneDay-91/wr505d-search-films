<script setup>
import { ref } from 'vue'

const monkeys =  ref([
  { hasEyesOpen: false }
])

const addMonkey = () => {
  monkeys.value.push({ hasEyesOpen: false })
}
</script>

<template>
  <div>
  <span @mouseover="monkey.hasEyesOpen = true" @mouseout="monkey.hasEyesOpen = false" v-for="monkey in monkeys" :key="monkey">
    {{ monkey.hasEyesOpen ? '🙉' : '🙈' }}
  </span>
    <br/>
    <button @click="addMonkey()">Add monkey</button>
  </div>
</template>

<style>span { font-size: 2rem; }</style>
