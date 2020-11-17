<template>
  <v-app>
    <Navbar />
    <AppBar />
    <v-main>
      <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>
import AppBar from '@/components/AppBar'
import Navbar from '@/components/Navbar'

export default {
  name: 'App',

  components: {
    AppBar,
    Navbar
  },

  data: () => ({
    //
  }),
};
</script>
