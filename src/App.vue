<template>
  <div style="position:absolute;top:0;left:0;width:100%;height:100vh;overflow:hidden;">
    <v-app>
      <Navbar />
      <AppBar />
      <v-main style="position:relative;width:100%;height:100vh;overflow:hidden;">
        <router-view></router-view>
      </v-main>
    </v-app>
  </div>
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
