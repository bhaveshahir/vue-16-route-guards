<template>
    <div>
      <h2>Login</h2>
      <button @click="login">Login</button>
    </div>
  </template>
  
  <script lang="ts">
  import { defineComponent } from 'vue'
  import { useRouter } from 'vue-router'
  
  export default defineComponent({
    setup() {
      const router = useRouter()
  
      const login = () => {
        localStorage.setItem('isLoggedIn', 'true')
        router.push('/dashboard')
      }
  
      return { login }
    }
  })
  </script>
  