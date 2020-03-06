<template>
  <v-app>

    <Drawer :drawer.sync="state.drawer" />
    <AppBar :drawer.sync="state.drawer" />

    <v-content>
      <router-view />
    </v-content>

    <Footer :app-name="appname" />

  </v-app>
</template>

<script>
import AppBar from '@/components/AppBar'
import Drawer from '@/components/Drawer'
import Footer from '@/components/Footer'

export default {
  name: 'App',

  components: {
    AppBar,
    Drawer,
    Footer
  },

  data: () => ({
    appname: 'MaMaPay',
    state: {
      drawer: false,
    }
    //
  }),
}
</script>
