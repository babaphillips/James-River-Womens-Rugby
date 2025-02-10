<template>
  <v-app>
    <!-- Navigation Drawer -->
    <v-navigation-drawer v-model="drawer" temporary app>
      <v-list color="logoColor">
        <v-list-item
          v-for="item in items"
          :key="item.value"
          :to="item.route"
          router
          link
        >
          <v-list-item-title>{{ item.text }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <!-- App Bar with Background Logo -->
    <v-app-bar color="logoColor" min-height="100px" app>
      <!-- Hamburger Icon to toggle the drawer -->
      <v-app-bar-nav-icon @click="drawer = !drawer" />
      <!-- Background Logo -->
      <v-img v-if="!mobile" :src="logo" cover class="ma-12" />
      <!-- For mobile screens -->
      <v-img v-else :src="logo" cover />
    </v-app-bar>

    <!-- Main Content Area -->
    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script setup>
import { ref } from "vue";
import { useDisplay } from "vuetify";
import logo from "../assets/JRWRFC BANNER.png";
const { mobile } = useDisplay();
const drawer = ref(false);

const items = ref([
  { text: "Home", value: "home", route: "/Home" },
  { text: "Schedule & Scores", value: "schedule", route: "/Schedule" },
  { text: "About", value: "about", route: "/About" },
  { text: "X Mas In July", value: "xmas", route: "/Xmas" },
  { text: "Join Us", value: "contact", route: "/Contact" },
]);
</script>

<style scoped>
.v-app-bar.v-toolbar {
  background-color: #092062;
}

.v-navigation-drawer {
  background-color: #092062;
}
</style>
