<template>
  <v-card flat class="ma-6 text-center" style="background-color: #029345">
    <v-row>
      <v-col cols="12"
        ><span class="text-overline textConfig">
          Welcome to the home of James River Women's Rugby Football Club
          (JRWRFC) !
          <br />
          No experience necessary!
          <br />
          <v-col cols="12" style="background-color: #029345"
            ><v-carousel hide-delimiters>
              <v-carousel-item :src="fallSchedule2024"></v-carousel-item>
              <v-carousel-item :src="promo1"></v-carousel-item>
              <v-carousel-item :src="promo2"></v-carousel-item>
              <v-carousel-item :src="promo3"></v-carousel-item> </v-carousel
          ></v-col>
          We embrace those who are knowledgeable or brand new to rugby. If you
          are interested in developing your skills or learning the first thing
          about rugby, we would love to meet you. As a team, we share a great
          camaraderie and love for this sport so we hope our enthusiasm is
          equally infectious.<br />
          Please make plans to come out and introduce yourself at our practices,
          matches, and/or socials.<br />
          All personalities, athletic conditions, and skill levels welcome. ​
          <br />
          <br />
          <nr></nr>Thank you for taking the time to visit our site! <br />
          New player looking for more info?
          <a
            style="color: #092062"
            href="https://drive.google.com/file/d/1CqQQONaCDBtOOluxSETrnha3UhLZovJN/view"
            target="_blank"
            rel="noopener noreferrer"
          >
            Click here
          </a>
          <br />
          Questions?
          <router-link to="/Contact" style="color: #092062"
            >Click here</router-link
          >
        </span></v-col
      >
    </v-row>
  </v-card>
</template>

<script setup>
import fallSchedule2024 from "../assets/FALL 24 PRACTICE (1).avif";
import promo1 from "../assets/3.avif";
import promo2 from "../assets/4.avif";
import promo3 from "../assets/5.avif";
</script>

<style scoped>
.textConfig {
  font-size: 1.2rem !important;
  font-weight: 400;
  color: #ffffff;
}
</style>
