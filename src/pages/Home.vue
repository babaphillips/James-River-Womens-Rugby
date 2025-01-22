<template>
  <v-card flat class="ma-8 text-center" style="background-color: #029345">
    <!-- Text header section -->
    <v-row>
      <v-col cols="12">
        <span class="textConfig">
          Welcome to the home of James River Women's Rugby Football Club!
        </span>
      </v-col>
    </v-row>

    <!-- Carousel Section -->
    <v-row class="">
      <v-col cols="12">
        <v-carousel hide-delimiters>
          <v-carousel-item
            :src="fallSchedule2024"
            alt="Fall 2024 Schedule"
          ></v-carousel-item>
          <v-carousel-item :src="promo1" alt="Promo 1"></v-carousel-item>
          <v-carousel-item :src="promo2" alt="Promo 2"></v-carousel-item>
          <v-carousel-item :src="promo3" alt="Promo 3"></v-carousel-item>
        </v-carousel>
      </v-col>
    </v-row>

    <!-- Text and Call to Action Section -->
    <v-row>
      <v-col cols="12">
        <span class="textConfig">
          We embrace those who are knowledgeable or brand new to rugby. If you
          are interested in developing your skills or learning the first thing
          about rugby, we would love to meet you.
          <br />
          <br />
          As a team, we share a great camaraderie and love for this sport so we
          hope our enthusiasm is equally infectious. <v-icon>mdi-heart</v-icon>
          <v-img
            :src="teampicture"
            class="mx-auto mt-1"
            width="300px"
            height="150px"
            cover
          />
          <br />

          Please make plans to come out and introduce yourself at our practices,
          matches, and/or socials.
          <br />
          <br />
          All personalities, athletic conditions, and skill levels welcome. ​
          <br /><br />

          Questions?
          <router-link to="/Contact" style="color: #092062"
            >Click here</router-link
          >
        </span>
      </v-col>
    </v-row>
  </v-card>
</template>

<script setup>
import fallSchedule2024 from "../assets/FALL 24 PRACTICE (1).avif";
import promo1 from "../assets/3.avif";
import promo2 from "../assets/4.avif";
import promo3 from "../assets/5.avif";
import teampicture from "../assets/54cada67-882f-4c3b-9bd2-54b7f25d90b5.jpeg";
</script>

<style scoped>
.v-carousel-item img {
  max-width: 100%; /* Ensure images in the carousel fit within the container */
  height: auto; /* Maintain aspect ratio */
}
</style>
