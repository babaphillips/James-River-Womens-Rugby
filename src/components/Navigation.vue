<template>
  <div class="logo">
    <!-- Logo -->

    <v-img :src="logo" max-height="100%" max-width="100%" cover></v-img>

    <!-- Tabs -->
    <v-tabs v-model="tab" scrollable grow>
      <v-tab
        v-for="item in items"
        :key="item.text"
        :style="{ color: tab === item.value ? '#092062' : '#ffffff' }"
        :text="item.text"
        :value="item.value"
        :to="item.route"
        class="text-lowercase pa-2"
      ></v-tab>
    </v-tabs>

    <!-- Tabs Window -->
    <v-tabs-window v-model="tab">
      <v-tabs-window-item
        v-for="item in items"
        :key="item.text"
        :value="item.value"
      >
      </v-tabs-window-item>
    </v-tabs-window>
  </div>
</template>

<script setup>
import logo from "../assets/JRWRFC BANNER.png";

const tab = ref("home"); // Default tab value

// Tab items with routes matching dynamically generated ones
const items = ref([
  { text: "Home", value: "home", route: "/Home" },
  { text: "Schedule & Scores", value: "schedule", route: "/Schedule" },
  { text: "About", value: "about", route: "/About" },
  { text: "X Mas In July", value: "xmas", route: "/Xmas" },
  { text: "Join Us", value: "contact", route: "/Contact" },
]);
</script>

<style scoped>
.logo {
  background-color: #029345;
}
</style>
