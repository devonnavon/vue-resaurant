<template>
  <v-card color="basil">
    <v-card-title class="text-center justify-center py-6">
      <h1 class="font-weight-bold display-3 basil--text">The Pond</h1>
    </v-card-title>

    <v-tabs v-model="tab" background-color="transparent" color="basil" grow>
      <v-tab v-for="item in items" :key="item.key" @click="tabClick(item)">{{ item.name }}</v-tab>
    </v-tabs>

    <v-tabs-items v-model="tab">
      <v-tab-item v-for="item in items" :key="item.key">
        <v-card color="basil" flat>
          <component :is="currentTab"></component>
        </v-card>
      </v-tab-item>
    </v-tabs-items>
  </v-card>
</template>


<script>
import About from "./About";
import Location from "./Location";
import Menu from "./Menu";

export default {
  components: {
    About: About,
    Location: Location,
    Menu: Menu
  },
  data() {
    return {
      tab: null,
      currentTab: "About",
      items: [
        {
          name: "About",
          key: 0
        },
        {
          name: "Location",
          key: 1
        },
        {
          name: "Menu",
          key: 2
        }
      ]
    };
  },
  methods: {
    tabClick: function(item) {
      this.currentTab = item.name;
    }
  }
};
</script>

<style>
.basil {
  background-color: #9c9c9c !important;
}
.basil--text {
  color: #202020 !important;
}

.v-card:not(.v-sheet--tile):not(.v-card--shaped) {
  border-top-left-radius: 1px !important;
  border-top-right-radius: 1px !important;
}

.theme--light {
  background-color: #9c9c9c !important;
}
/* 
.koi {
  background-image: koi !important;
} */
</style>

