<template>
  <v-card flat class="ma-12">
    <v-row>
      <v-col cols="12" class="bg-white"
        ><span class="text-h6 text-green-darken-3">
          We embrace those who are knowledgeable or brand new to rugby. If you
          are interested in developing your skills or learning the first thing
          about rugby, we would love to meet you. As a team, we share a great
          camaraderie and love for this sport so we hope our enthusiasm is
          equally infectious. Please make plans to come out and introduce
          yourself at our practices, matches, and/or socials. All personalities,
          athletic conditions, and skill levels welcome. ​ Thank you for taking
          the time to visit our site!</span
        ></v-col
      ><v-col cols="12" class="bg-white"
        ><v-carousel hide-delimiters>
          <v-carousel-item :src="fallSchedule2024"></v-carousel-item>

          <v-carousel-item
            src="https://cdn.vuetifyjs.com/images/cards/hotel.jpg"
            cover
          ></v-carousel-item> </v-carousel
      ></v-col>
    </v-row>
  </v-card>
</template>

<script setup>
import fallSchedule2024 from "../assets/FALL 24 PRACTICE (1).avif";
</script>
