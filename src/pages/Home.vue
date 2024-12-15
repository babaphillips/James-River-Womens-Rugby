<template>
  <v-card class="mx-auto bg-white border elevation-0" hover>
    <v-card-item>
      <v-card-title class="text-center">
        Welcome To The Home Of James River Women's Rugby Football Club (JRWRFC)
      </v-card-title>

      <v-card-subtitle class="text-center">
        No experience necessary!</v-card-subtitle
      >
    </v-card-item>

    <v-card-text>
      <v-row>
        <v-col cols="6">
          <v-img
            :src="fallSchedule2024"
            max-height="100%"
            max-width="100%"
            cover
          ></v-img
        ></v-col>
        <v-col cols="6"
          ><span>
            We embrace those who are knowledgeable or brand new to rugby. If you
            are interested in developing your skills or learning the first thing
            about rugby, we would love to meet you. As a team, we share a great
            camaraderie and love for this sport so we hope our enthusiasm is
            equally infectious. Please make plans to come out and introduce
            yourself at our practices, matches, and/or socials. All
            personalities, athletic conditions, and skill levels welcome. ​
            Thank you for taking the time to visit our site!</span
          ></v-col
        >
      </v-row>

      <span></span>
    </v-card-text>
  </v-card>
</template>

<script setup>
import fallSchedule2024 from "../assets/FALL 24 PRACTICE (1).avif";
</script>
