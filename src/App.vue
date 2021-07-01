<template>
  <v-app id="inspire" class="aber">
    <v-navigation-drawer
      v-model="drawer"
      app>

      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="text-h6">
            Welcome
          </v-list-item-title>
          <v-list-item-subtitle>
            Joan Wilkins
          </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list
        dense
        nav>

        <v-list-item
          v-for="item in items"
          :key="item.title"
          :to="item.to"
          link>
          
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar app
      color="white"
      flat
    >

      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title> 
        <v-img
          left
          :src="require('./assets/Base_Logo.png')"
          class="my-3"
          contain
        />
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-img
          :src="require('./assets/Group_2.png')"
          max-width="130"
      />
    </v-app-bar>

    <v-main>
      <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>
  export default {
    data: () => ({ 
      drawer: null,
      items: [
          { title: 'Overview', icon: 'mdi-view-dashboard', to: '/' },
          { title: 'Analytics', icon: 'mdi-access-point', to: '/' },
          { title: 'Vehicles', icon: 'mdi-car', to: '/vehicles' },
          { title: 'Service', icon: 'mdi-car-cog', to: '/' },
          { title: 'Map', icon: 'mdi-map', to: '/' },
          { title: 'Chat', icon: 'mdi-chat', to: '/' },
          { title: 'Settings', icon: 'mdi-cog-outline', to: '/' },
        ],
    }),
  }
</script>

<style>
  .aber{
    width: auto;
    background-color: #f4f6fc;

  }
</style>