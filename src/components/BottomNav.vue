<template>
<v-app id="app">
  <div id="bottom-nav" >
    <v-card height="100%" flat >
        <v-bottom-nav
        :active.sync="bottomNav"
        :value="true"
        absolute
        color="transparent"
        >
        <v-btn
            color="teal"
            flat
            value="recent"
        >
            <span>History</span>
            <v-icon>history</v-icon>
        </v-btn>

        <v-btn
            to="CreateTrade"
            color="teal"
            flat
            value="favorites"
        >
            <span>Add</span>
            <v-icon>fas fa-plus-circle</v-icon>
        </v-btn>

        <v-btn
            color="teal"
            flat
            value="nearby"
        >
            <span>Nearby</span>
            <v-icon>place</v-icon>
        </v-btn>
        </v-bottom-nav>
    </v-card>
  </div>
</v-app>
</template>

<script>
  export default {
    data () {
      return {
        bottomNav: 'history'
      }
    }
  }
</script>

<style scoped>
 /* BottomNavを固定CSS */
 #bottom-nav {
    width: 100%;
    position: fixed;
    bottom: 0;
    z-index:999;
  } 
  
</style>
