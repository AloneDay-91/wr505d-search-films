<script setup>
import { ref } from 'vue'

const title = 'Authentification'

const email = ref('toto@mail.com')
const password = ref('1234')

</script>

<template>
  <div id="login-form">
    <form @submit.prevent="loggedIn = true">
      <h1>{{ title }}</h1>
      <p>Remplissez ce formulaire pour vous connecter.</p>
      <hr />

      <label for="email"><b>Email</b></label>
      <input
        type="text"
        v-model="email"
        placeholder="Entrez votre courriel"
        id="email"
        name="email"
        required
      />

      <label for="psw"><b>Mot de passe</b></label>
      <input
        type="password"
        v-model="password"
        placeholder="Entrez votre mot de passe"
        id="psw"
        name="psw"
        required
      />

      <p><button type="submit">Se connecter</button></p>
    </form>
  </div>
  <div v-if="loggedIn === true">
  </div>
</template>
