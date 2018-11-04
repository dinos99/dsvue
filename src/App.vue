<template>
  <div id="app">
    <v-app id="inspire">
        <v-toolbar
          dark
          color="primary"
          dense
          clipped-left
          flat
        >
            <v-toolbar-side-icon></v-toolbar-side-icon>
            <v-toolbar-title class="ml-0 pl-3 white--text">
                <div class="title">dsVue v1.0</div>
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
      <router-view/>
    </v-app>
  </div>
</template>

<script>
import dsHeader from '@/components/frameset/dsHeader'
export default {
  name: 'App',
  components: {
    dsHeader
  }
}
</script>

<style>
.title {width: 240px;}
#app { width: 100%; margin:0; padding:0; }
</style>
