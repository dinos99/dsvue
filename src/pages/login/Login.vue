<template>
  <v-app
    id="inspire"
  >
    <v-navigation-drawer
      v-model="drawer"
      fixed
      clipped
      app
    >
      <v-list dense>
        <v-list-tile v-for="item in items" :key="item.text" @click="">
          <v-list-tile-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>
              {{ item.text }}
            </v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        <v-subheader class="mt-3 grey--text text--darken-1">SUBSCRIPTIONS</v-subheader>
        <v-list>
          <v-list-tile v-for="item in items2" :key="item.text" avatar @click="">
            <v-list-tile-avatar>
              <img :src="`https://randomuser.me/api/portraits/men/${item.picture}.jpg`" alt="">
            </v-list-tile-avatar>
            <v-list-tile-title v-text="item.text"></v-list-tile-title>
          </v-list-tile>
        </v-list>
        <v-list-tile class="mt-3" @click="">
          <v-list-tile-action>
            <v-icon color="grey darken-1">add_circle_outline</v-icon>
          </v-list-tile-action>
          <v-list-tile-title class="grey--text text--darken-1">Browse Channels</v-list-tile-title>
        </v-list-tile>
        <v-list-tile @click="">
          <v-list-tile-action>
            <v-icon color="grey darken-1">settings</v-icon>
          </v-list-tile-action>
          <v-list-tile-title class="grey--text text--darken-1">Manage Subscriptions</v-list-tile-title>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
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
    <v-content>
      <v-container fill-height >
        <v-layout justify-center align-center>
            <v-card width="420px">
                <v-toolbar color="primary" class="white--text" flat>
                    <v-toolbar-title>Login</v-toolbar-title>
                    <v-spacer></v-spacer>
                </v-toolbar>
                <v-container
                    fluid
                    grid-list-lg
                >
                    <v-layout row wrap>
                        <v-flex xs12>
                            <v-card-text>
                                <v-form>
                                    <v-text-field prepend-icon="person" name="login" label="Login" type="text"></v-text-field>
                                    <v-text-field id="password" prepend-icon="lock" name="password" label="Password" type="password"></v-text-field>
                                </v-form>
                            </v-card-text>
                            <v-card-actions>
                                <v-spacer></v-spacer>
                                <v-btn depressed small color="primary">Login</v-btn>
                            </v-card-actions>
                        </v-flex>
                    </v-layout>
                </v-container>
            </v-card>
        </v-layout>
      </v-container>
    </v-content>
    <v-footer app fixed>
      <span>&copy; 2017</span>
    </v-footer>
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