<template>
    <v-layout>
        <v-content>
      <section>
        <v-parallax src="static/business-computer-connection-450035.jpg" height="600" width="100%">
          <v-container justify-center>
            <v-layout column class="white--text" style="align-items: center;">
              <img xsclass="item" src="static/jorge's profile.png" alt="Vuetify.js" height="200" width="200">
              <h1 class="item white--text mb-2 display-2 text-xs-center font-weight-medium" id=name>Jorge Castano</h1>
              <div class="item subheading mb-3 text-xs-center display-4">Software developer</div>
            </v-layout>
          </v-container>
        </v-parallax>
      </section>
      <section>
        <v-layout column wrap class="my-5" align-center >
          <v-flex xs12 sm4 class="my-3">
            <div class="text-xs-center">
              <h2 class="headline" >The best way to start developing</h2>
              <span class="subheading">
                Cras facilisis mi vitae nunc
              </span>
            </div>
          </v-flex>
          <v-flex xs12>
            <v-container grid-list-xl>
              <v-layout row wrap align-center>
                <v-flex xs12 md4>
                  <v-card class="elevation-0 transparent">
                    <v-card-text class="text-xs-center">
                      <v-icon x-large class="blue--text text--lighten-2">important_devices</v-icon>
                    </v-card-text>
                    <v-card-title primary-title class="layout justify-center">
                      <div class="headline text-xs-center">Programming</div>
                    </v-card-title>
                    <v-card-text>
                      Finding the right tool to create a solution is my passion. Progressing technological requirements require innovative solutions. Curiosity and creativity guide my discovery process and allow for the innovation to tackle the constantly shifting technological market.
                    </v-card-text>
                  </v-card>
                </v-flex>
                <v-flex xs12 md4>
                  <v-card class="elevation-0 transparent">
                    <v-card-text class="text-xs-center">
                      <v-icon x-large class="blue--text text--lighten-2">memory</v-icon>
                    </v-card-text>
                    <v-card-title primary-title class="layout justify-center">
                      <div class="headline">Home automation</div>
                    </v-card-title>
                    <v-card-text>
                      Cras facilisis mi vitae nunc lobortis pharetra. Nulla volutpat tincidunt ornare.
                      Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.
                      Nullam in aliquet odio. Aliquam eu est vitae tellus bibendum tincidunt. Suspendisse potenti.
                    </v-card-text>
                  </v-card>
                </v-flex>
                <v-flex xs12 md4>
                  <v-card class="elevation-0 transparent">
                    <v-card-text class="text-xs-center">
                      <v-icon x-large class="blue--text text--lighten-2">build</v-icon>
                    </v-card-text>
                    <v-card-title primary-title class="layout justify-center">
                      <div class="headline text-xs-center">Hobbies</div>
                    </v-card-title>
                    <v-card-text>
                      Cras facilisis mi vitae nunc lobortis pharetra. Nulla volutpat tincidunt ornare.
                      Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.
                      Nullam in aliquet odio. Aliquam eu est vitae tellus bibendum tincidunt. Suspendisse potenti.
                    </v-card-text>
                  </v-card>
                </v-flex>
              </v-layout>
            </v-container>
          </v-flex>
        </v-layout>
      </section>

      <section>
        <v-parallax src="assets/section.jpg" height="380">
          <v-layout column align-center justify-center>
            <div class="headline white--text mb-3 text-xs-center">Web development has never been easier</div>
            <em>Kick-start your application today</em>
            <v-btn
              class="blue lighten-2 mt-5"
              dark
              large
              href="/pre-made-themes"
            >
              Get Started
            </v-btn>
          </v-layout>
        </v-parallax>
      </section>

      <section>
        <v-container grid-list-xl>
          <v-layout row wrap justify-center class="my-5">
            <v-flex xs12 sm4>
              <v-card class="elevation-0 transparent">
                <v-card-title primary-title class="layout justify-center">
                  <div class="headline">Company info</div>
                </v-card-title>
                <v-card-text>
                  Cras facilisis mi vitae nunc lobortis pharetra. Nulla volutpat tincidunt ornare.
                  Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.
                  Nullam in aliquet odio. Aliquam eu est vitae tellus bibendum tincidunt. Suspendisse potenti.
                </v-card-text>
              </v-card>
            </v-flex>
            <v-flex xs12 sm4 offset-sm1>
              <v-card class="elevation-0 transparent">
                <v-card-title primary-title class="layout justify-center">
                  <div class="headline">Contact us</div>
                </v-card-title>
                <v-card-text>
                  Cras facilisis mi vitae nunc lobortis pharetra. Nulla volutpat tincidunt ornare.
                </v-card-text>
                <v-list class="transparent">
                  <v-list-item-title>
                    <v-list-item-action>
                      <v-icon class="blue--text text--lighten-2">place</v-icon>
                    </v-list-item-action>
                    <v-list-item-content>
                      <v-list-item-title>Calgary, Canada</v-list-item-title>
                    </v-list-item-content>
                  </v-list-item-title>
                  <v-list-item-title>
                    <v-list-item-action>
                      <v-icon class="blue--text text--lighten-2">email</v-icon>
                    </v-list-item-action>
                    <v-list-item-content>
                      <v-list-item-title>jcast236@mtroyal.ca</v-list-item-title>
                    </v-list-item-content>
                  </v-list-item-title>
                </v-list>
              </v-card>
            </v-flex>
          </v-layout>
        </v-container>
      </section>

      <v-footer>
        <v-layout row wrap align-center>
          <v-flex xs12>
          </v-flex>
        </v-layout>
      </v-footer>
    </v-content>

    </v-layout>
</template>
<script>
export default {
  name: 'MainContainer',
  data () {
    return {
      title: 'Your Logo'
    }
  }
}
</script>
<style scoped>
h1, h2 {
    font-weight: normal;
}
ul {
    list-style-type: none;
    padding: 0;
}
li {
    display: inline-block;
    margin: 0 10px;
}
a {
    color: #42b983;
}
#name{
    text-shadow: 0 1px 0 #ccc,
        0 2px 0 #c9c9c9,
        0 3px 0 #bbb,
        /* 0 4px 0 #b9b9b9,
        0 5px 0 #aaa, */
        /* 0 6px 1px rgba(0,0,0,.1), */
        0 0 5px rgba(0,0,0,.1),
        0 1px 3px rgba(0,0,0,.3),
        0 3px 5px rgba(0,0,0,.2),
        0 5px 10px rgba(0,0,0,.25),
        0 10px 10px rgba(0,0,0,.2),
        0 15px 15px rgba(0,0,0,.15);
}
</style>
