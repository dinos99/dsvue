<template>
  <div id="app">
    <v-app id="inspire" dark>
      <v-toolbar
        dark
        color="primary"
        dense
        clipped-left
        flat
      >
          <v-toolbar-side-icon @click.stop="display.sidemenu = !display.sidemenu"></v-toolbar-side-icon>
          <v-toolbar-title :style="'width:340px;'" class="ml-0 pl-1 pr-3 white--text">
              <div class="title">다구형 놀이터 v1.0</div>
          </v-toolbar-title>
          <ds-header></ds-header>
          <v-spacer></v-spacer> 
          <v-avatar size="30" class="pr-3">
              <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John">
          </v-avatar>
          <div>dojun8ho@gmail.com</div>
          <!--
          <v-btn depressed small color="primary">Login</v-btn>
          <v-btn icon><v-icon>search</v-icon></v-btn>
          <v-btn icon><v-icon>refresh</v-icon></v-btn>
          -->
          <v-btn icon><v-icon>notifications</v-icon></v-btn>
          <v-btn icon><v-icon>apps</v-icon></v-btn>
          <v-btn icon><v-icon>more_vert</v-icon></v-btn>
      </v-toolbar>
      <ds-side-menu
        :drawer="display.sidemenu">
      </ds-side-menu>
      <router-view/>
    </v-app>
  </div>
</template>

<script>
import dsHeader from '@/components/frameset/dsHeader'
import dsSideMenu from '@/components/frameset/dsSideMenu'
export default {
  name: 'App',
  components: {
    dsHeader,
    dsSideMenu
  },
  data: () => ({
    display: {
      sidemenu: null
    }
  })
}
</script>

<style>
.title {font-family: 'Nanum Gothic' !important; font-weight: bold;}
</style>
