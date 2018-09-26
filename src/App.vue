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
          <v-list-tile avatar @click="drawer=!drawer">
            <v-list-tile-avatar>
              <img src="static/jorge's profile.png" alt="Avatar">
            </v-list-tile-avatar>

            <v-list-tile-content>
              <v-list-tile-title>Jorge Castano</v-list-tile-title>
            </v-list-tile-content>
          </v-list-tile>
        </v-list>
      <v-divider></v-divider>
      <v-list>
        <v-list-tile
          value="true"
          v-for="(item, i) in items"
          :key="i"
        >
          <v-list-tile-action>
            <v-icon v-html="item.icon"></v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title v-text="item.title"></v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar app class="white" :clipped-left="clipped">
      <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
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
      <!-- <v-toolbar-side-icon>
        <v-flex>
            <v-avatar size="36px">
            </v-avatar>
          </v-flex>
      </v-toolbar-side-icon> -->
      <v-toolbar-side-icon>
        <v-flex>
            <v-avatar size="36px" id=githubContainer>
              <i id=github class="fab fa-github" size="36px"></i>
            </v-avatar>
          </v-flex>
      </v-toolbar-side-icon>

    </v-toolbar>
    <router-view/>
    <v-navigation-drawer temporary 
      :right="right"
      v-model="rightDrawer"
      fixed
      app
    >
      <v-list>
        <v-list-tile @click="right = !right">
          <v-list-tile-action>
            <v-icon>compare_arrows</v-icon>
          </v-list-tile-action>
          <v-list-tile-title>Switch drawer (click me)</v-list-tile-title>
        </v-list-tile>
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
            rightDrawer: false,
        }
    }
}
</script>
<style scoped>
#githubContainer{
  font-size: 36px;
}
</style>