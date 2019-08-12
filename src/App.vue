<template>
  <div id="app">
    <v-navigation-drawer
      persistent
      :mini-variant="miniVariant"
      :clipped="clipped"
      v-model="drawer"
      enable-resize-watcher
      fixed
      app
      :width="200"
    >
      <v-list>
          <v-list-item @click="drawer=!drawer">
            <v-list-item-avatar>
              <img src="static/jorge's profile.png" alt="Avatar">
            </v-list-item-avatar>

            <v-list-item-content>
              <v-list-item-title>Jorge Castano</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      <v-divider></v-divider>
      <v-list>
        <v-list-item
          value="true"
          v-for="(item, i) in items"
          :key="i"
        >
          <v-list-item-action>
            <v-icon v-html="item.icon"></v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      app
      dense
      shrink-on-scroll
      fade-img-on-scroll
      dark
      src="static/business-computer-connection-450035.jpg"
      scroll-threshold="300"

    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <!-- <v-btn icon @click.stop="miniVariant = !miniVariant">
        <v-icon v-html="miniVariant ? 'chevron_right' : 'chevron_left'"></v-icon>
      </v-btn>
      <v-btn icon @click.stop="clipped = !clipped">
        <v-icon>web</v-icon>
      </v-btn>
      <v-btn icon @click.stop="fixed = !fixed">
        <v-icon>remove</v-icon>
      </v-btn> -->
      <v-toolbar-title v-text="title"></v-toolbar-title>
      <v-spacer></v-spacer>
      <!-- <v-btn icon @click.stop="rightDrawer = !rightDrawer">
        <v-icon>menu</v-icon>
      </v-btn> -->
      <!-- <v-app-bar-nav-icon>
        <v-flex>
            <v-avatar size="36px">
            </v-avatar>
          </v-flex>
      </v-app-bar-nav-icon> -->
      <v-app-bar-nav-icon>
        <v-flex>
            <v-avatar size="36px" id=githubContainer>
              <i id=github class="fab fa-github" size="36px"></i>
            </v-avatar>
          </v-flex>
      </v-app-bar-nav-icon>

    </v-app-bar>
    <router-view/>
    <v-navigation-drawer temporary
      :right="right"
      v-model="rightDrawer"
      fixed
      app
    >
      <v-list>
        <v-list-item @click="right = !right">
          <v-list-item-action>
            <v-icon>compare_arrows</v-icon>
          </v-list-item-action>
          <v-list-item-title>Switch drawer (click me)</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      title: 'Jorge Castano\'s',
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {icon: 'dashboard', title: 'Dashboard'},
        {icon: 'fas fa-briefcase', title: 'Projects'},
        {icon: 'fab fa-fort-awesome-alt', title: 'Hobbies'},
        {icon: 'far fa-file-pdf', title: 'Resume'}
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false
    }
  }
}
</script>
<style scoped>
#githubContainer{
  font-size: 36px;
}
</style>
