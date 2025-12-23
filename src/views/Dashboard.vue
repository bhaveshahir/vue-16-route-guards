<template>
    <div>
      <h2>Dashboard (Protected)</h2>
      <button @click="logout">Logout</button>
    </div>
  </template>
  
  <script lang="ts">
  import { defineComponent } from 'vue'
  import { useRouter } from 'vue-router'
  
  export default defineComponent({
    setup() {
      const router = useRouter()
  
      const logout = () => {
        localStorage.removeItem('isLoggedIn')
        router.push('/login')
      }
  
      return { logout }
    }
  })
  </script>
  