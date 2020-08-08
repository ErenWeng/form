<template>
  <v-app>
    <Login/>
  </v-app>
</template>

<script>
import Login from './components/Authentication/Login'

export default {
  name: 'App',
  components: {
    Login
  }
}
</script>
