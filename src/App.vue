<template>
  <v-app>
    <v-app-bar
      app
      color="black"
      height="100"
      dark
    >
      <v-container fluid class="pa-0">
        <v-row no-gutters>
          <v-col key="1" cols="2"></v-col>
          <v-col key="2" cols="8">
            <v-row class="white--text headline">
              <span>Vuetify</span><span class="font-weight-light">Sample</span>
              <v-spacer></v-spacer>
            </v-row>
          </v-col>
          <v-col cols="2" key="3"></v-col>
        </v-row>
      </v-container>
    </v-app-bar>

    <v-content>
      <HelloWorld/>
    </v-content>

    <v-footer app color="black" height="47px">
      <v-container fluid class="pa-0">
        <v-row no-gutters>
          <v-col key="1" cols="2"></v-col>
          <v-col key="2" cols="8">
            <v-row class="white--text caption">
              <span>Claus Straube</span>
              <v-spacer></v-spacer>
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

}
</script>
