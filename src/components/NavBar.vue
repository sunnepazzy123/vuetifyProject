<template>
  <nav>
     <v-app-bar color="deep-purple accent-4" dense dark >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>Courier Service</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn color="red">
        <span>Login</span>
        <v-icon right>mdi-login</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-logout</v-icon>
      </v-btn>
       </v-app-bar>

        <v-navigation-drawer app v-model="drawer">
        <v-list nav dense >
        <v-list-item
          active-class="deep-purple--text text--accent-4"
           v-for="item in items"
            :key="item.title"
             link
        >
            <v-list-item-icon>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-icon>
          <v-list-item>
            <v-list-item-content>{{ item.title }}</v-list-item-content>
          </v-list-item>
        </v-list-item>
      </v-list>

      </v-navigation-drawer>

  </nav>
</template>

<script>
export default {

  data(){
    return {
      drawer: false,
      items: [
          { title: 'Home', icon: 'mdi-view-dashboard' },
          { title: 'About', icon: 'mdi-forum' },
        ],

    }
  }

}
</script>

<style>

</style>