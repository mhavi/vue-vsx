<template>
  <v-app id="app">
    <app-zones v-if="['/'].indexOf($route.name) > -1"></app-zones>
    <v-content>
      <!-- not needed -->
      <!-- router-view></router-view -->
      <v-container fill-height>
        <v-layout align-space-around justify-center fill-height column>
          <v-card dark color="primary" flat height="50%">
          <div class="text-xs-center">
            <v-btn fab dark large color="purple">
              <v-icon>add</v-icon>
            </v-btn>
            <div class="power">up</div>
          </div>
         </v-card>
         <v-card dark color="secondary" flat height="50%">
          <div class="text-xs-center">
            <v-btn fab dark large color="blue">
              <v-icon>add</v-icon>
            </v-btn>
            <div class="power">down</div>
          </div>
        </v-card>
        </v-layout>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
import AppZones from '@/components/AppZones';

export default {
  name: 'App',
  components: {
      AppZones
  }
}
</script>
<style scoped>
.content-container {
  margin: auto;
  height: 50vh;
}
.power {
  position: absolute;
  top: 50%;
  left: 50%;
}
</style>
