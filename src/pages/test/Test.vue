<template>
<v-app id="inspire">
    <v-toolbar
        dark
        color="primary"
        dense
        fixed
        clipped-left
        app
        flat
    >
        <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
        <v-toolbar-title class="ml-0 pl-3 white--text">
            <span class="title">dsVue v1.0</span>
        </v-toolbar-title>
        <v-spacer></v-spacer> 
        <v-avatar size="30">
            <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John">
        </v-avatar>
        <div style="padding-left:5px;">dojun8ho@gmail.com</div>
        <v-btn icon><v-icon>search</v-icon></v-btn>
        <v-btn icon><v-icon>apps</v-icon></v-btn>
        <v-btn icon><v-icon>refresh</v-icon></v-btn>
        <v-btn icon><v-icon>more_vert</v-icon></v-btn>
    </v-toolbar>
</v-app>
</template>
<script>
 export default {
    data: () => ({
      drawer: null,
      items: [
        { icon: 'trending_up', text: 'Most Popular' },
        { icon: 'subscriptions', text: 'Subscriptions' },
        { icon: 'history', text: 'History' },
        { icon: 'featured_play_list', text: 'Playlists' },
        { icon: 'watch_later', text: 'Watch Later' }
      ],
      items2: [
        { picture: 28, text: 'Joseph' },
        { picture: 38, text: 'Apple' },
        { picture: 48, text: 'Xbox Ahoy' },
        { picture: 58, text: 'Nokia' },
        { picture: 78, text: 'MKBHD' }
      ]
    }),
    props: {
      source: String
    }
  }
</script>

<style>
.color{color:#ff0077}
</style>