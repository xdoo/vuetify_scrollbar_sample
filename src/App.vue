<template>
  <v-app>
    <v-app-bar
      app
      color="black"
      height="100"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />

        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        />
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-content>
      <HelloWorld/>
    </v-content>

    <v-footer app color="black" height="47px">
      <v-container fluid class="pa-0">
        <v-row no-gutters>
          <v-col key="1" cols="2"></v-col>
          <v-col key="2" cols="8">
            <v-row class="white--text">
              <span>{{screenHeigth}}</span>
              <v-spacer></v-spacer>
              <span>foo</span>
            </v-row>
          </v-col>
          <v-col cols="2" key="3"></v-col>
        </v-row>
      </v-container>
    </v-footer>
  </v-app>
</template>

<script lang="ts">
import Vue from 'vue'
import { Component } from 'vue-property-decorator'
import HelloWorld from './components/HelloWorld.vue'

@Component({
  components: {
    HelloWorld
  }
})
export default class App extends Vue{

  get screenHeigth() {
    return this.$vuetify.breakpoint.height
  }

}
</script>
