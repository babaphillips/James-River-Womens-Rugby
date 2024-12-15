<template>
  <v-card
    class="bg-white"
    :style="{
      backgroundImage: `url(${logo})`,
      backgroundSize: 'cover',
      backgroundPosition: 'center',
      backgroundRepeat: 'no-repeat',
    }"
  >
    <!-- <v-img class="bg-grey-lighten-2" :src="logo" cover></v-img> -->
    <v-card-title class="text-center justify-center py-6">
      <!-- <h1 class="font-weight-bold text-h2 text-basil">
        James River Womens Rugby
      </h1> -->
    </v-card-title>

    <!-- Tabs -->
    <v-tabs v-model="tab" grow>
      <v-tab
        v-for="item in items"
        color="blue-darken-4"
        :key="item.text"
        :text="item.text"
        :value="item.value"
        :to="item.route"
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
  </v-card>
</template>

<script setup>
import logo from "../assets/JRWRFC_Crest.png";

const tab = ref("home"); // Default tab value

// Tab items with routes matching dynamically generated ones
const items = ref([
  { text: "Home", value: "home", route: "/Home" },
  { text: "Contact", value: "contact", route: "/Contact" },
  { text: "About", value: "about", route: "/About" },
  { text: "X Mas In July", value: "xmas", route: "/Xmas" },
]);
</script>
<style scoped>
.card-with-background {
  background-image: url("../assets/JRWRFC_Crest.png"); /* or use logoURL dynamically */
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}
</style>
