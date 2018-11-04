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
            <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
            <v-toolbar-title class="ml-0 pl-3 white--text">
                <span class="title">dsVue v1.0</span>
            </v-toolbar-title>
            <v-spacer></v-spacer> 
            <!--
            <v-avatar size="30">
                <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John">
            </v-avatar>
            <div style="padding-left:5px;">dojun8ho@gmail.com</div>
            <v-btn depressed small color="primary">Login</v-btn>
            <v-btn icon><v-icon>search</v-icon></v-btn>
            <v-btn icon><v-icon>apps</v-icon></v-btn>
            <v-btn icon><v-icon>refresh</v-icon></v-btn>
            <v-btn icon><v-icon>more_vert</v-icon></v-btn>
            -->
            <v-btn depressed small flat>Login</v-btn>
        </v-toolbar>
      <router-view/>
    </v-app>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
.v-toolbar {
  width:  1024px; margin:0 auto;
}
#app { width: 100%; margin:0; padding:0; }
#inspire { width:1024px; margin:0 auto; padding:0;}
</style>
