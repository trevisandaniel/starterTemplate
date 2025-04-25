<template>
  <div class="max-w-sm mx-auto mt-10">
    <h1 class="text-xl font-bold mb-4">Login</h1>
    <form @submit.prevent="login">
      <input v-model="email" type="email" placeholder="Email" class="w-full p-2 border rounded mb-2" />
      <input v-model="password" type="password" placeholder="Senha" class="w-full p-2 border rounded mb-2" />
      <button class="w-full bg-blue-600 text-white p-2 rounded">Entrar</button>
    </form>
    <p v-if="message" class="text-red-500 mt-2">{{ message }}</p>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const email = ref('')
const password = ref('')
const message = ref('')

function login() {
  if (email.value === 'admin@teste.com' && password.value === '123456') {
    message.value = ''
    alert('Login bem-sucedido!')
  } else {
    message.value = 'Credenciais inválidas'
  }
}
</script>
