<template>
  <v-container fluid class="pa-0">
    <v-img
      :src="require('@/assets/oberbayern.jpg')"
      :lazy-src="require('@/assets/oberbayern_pre.jpg')"
      :height="bgHeigth"
    > 
      <v-sheet
        color="transparent"
        :height="bgHeigth"
        class="overflow-y-auto"
        :max-height="bgHeigth"
      >
      <v-row no-gutters align="start">
        <v-col key="1" cols="2"></v-col>
        <v-col key="2" cols="8">
          <v-card
            class="my-10"
          >
            <v-toolbar color="grey darken-3" height="80px">
              <v-container fluid class="pa-0">
                <v-row no-gutters class="mt-12 white--text">
                  <h1 class="headline">XRechnung validieren und visualisieren</h1>
                </v-row>
              </v-container>
            </v-toolbar>
            <v-toolbar color="grey darken-4" class="white--text" height="60px">
              <span>{{count}} on {{listHeight}}px</span>
            </v-toolbar>
            
              <v-list>
              <v-list-item
                v-for="i in count"
                :key="i"
                dark
                class="black--text"
              >
                <v-list-item-icon>
                  <v-icon class="black--text">mdi-file</v-icon>
                </v-list-item-icon>
                <v-list-item-content>
                  <v-list-item-title class="black--text">Foo Item {{i}}</v-list-item-title>
                  <v-list-item-subtitle class="black--text">The subtitle for the... Foo</v-list-item-subtitle>
                </v-list-item-content>
                <v-list-item-action >
                  <v-icon class="black--text">mdi-cloud-download</v-icon>
                </v-list-item-action>
                </v-list-item>
              </v-list>
          </v-card>
        </v-col>
        <v-col cols="2" key="3"></v-col>
      </v-row>
      </v-sheet>
    </v-img>
  </v-container>
</template>

<script lang="ts">
import Vue from 'vue'
import { Component } from 'vue-property-decorator'

@Component
export default class Helloworld extends Vue {
 
  count: number = 100

  get bgHeigth() {
    return this.$vuetify.breakpoint.height - 147
  }

  get cardHeight() {
    return this.$vuetify.breakpoint.height - 147 - 60
  }

  get listHeight() {
    return this.$vuetify.breakpoint.height - 147 - 60 - 140 - 5
  }

}
</script>
