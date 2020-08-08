<template>
  <v-app>
    <!-- <Login/> -->
    <Signup/>
  </v-app>
</template>

<script>
import Signup from './components/Authentication/Signup'

export default {
  name: 'App',
  components: {
    Signup
  }
}
</script>
