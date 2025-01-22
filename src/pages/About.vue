<!-- <template>
  <v-card class="text-center" flat style="background-color: #029345"
    ><v-card-title class="mt-4 mb-4">JRW History</v-card-title>
    <span>
      <a
        href="https://www.dropbox.com/scl/fi/7h2i1p57et9zxtxf3g25b/James-River-Women-s-Constitution-_-Revised-Feb-2021.pdf?rlkey=cr76b1gjd9bnfhmtkv8rrhpkd&e=1&dl=0"
        target="_blank"
        rel="noopener noreferrer"
        style="color: #092062"
      >
        CLICK HERE TO VIEW THE JRW CONSTITUTION
      </a> </span
    ><v-card-text
      >Stephanie H. Edwards (Stephie-Jo) formed James River Women’s Rugby
      Football Club (JWRFC) in the Spring of 2001. Before that, there was not a
      women’s club team in Richmond, VA. <br />With the assistance of the James
      River Men’s and United Men’s RFC, JRWRFC was able to gather interested
      players from the area. Enough players came out to establish the need to
      schedule practices. With the enthusiasm of these new players, James River
      entered a team in the Cape Fear Sevens Tournament that summer.<br />
      There was a positive reaction from the players to continue with a team in
      the fall. James River Men’s RFC, our established brother club, allowed us
      to use a portion of their field and assisted in coaching the new players
      during the fall season. <br />
      Schedule practices began in mid-August and continued through the first
      part of November. Eight scheduled matches were played and several
      scrimmages with Virginia Commonwealth University Women’s Football Club
      were organized and executed. The team also participated in the Sandy Lee
      State Cup in late October. After a successful trial run, the women decided
      to move forward with the club.<br />
      On January 15, 2002, the club held its inaugural Annual General Meeting
      (AGM). The club voted in Shannon Plum as the newly elected president; as
      well as, its first executive board. </v-card-text
    ><span class="text-overline textConfig font-weight-bold"
      >Bleed Blue and Green!
    </span></v-card
  >
</template> -->

<template>
  <div>
    <v-col cols="12" md="12" class="d-flex justify-center">
      <v-card class="bg-transparent" flat>
        <v-card-title class="text-center"> The 2025 JRW Board </v-card-title>

        <v-row class="d-flex justify-center mb-4">
          <!-- Loop through board members -->
          <v-col
            v-for="(member, index) in boardMembers"
            :key="index"
            cols="6"
            sm="6"
            md="3"
            class="d-flex justify-center"
          >
            <v-card
              class="text-center board-card bg-white"
              height="200px"
              width="250px"
              elevation="12"
            >
              <!-- Profile Image -->
              <v-img
                :src="member.photo"
                class="mx-auto mt-1"
                width="100px"
                height="100px"
                cover
              />
              <v-card-title>{{ member.name }}</v-card-title>
              <v-card-subtitle>{{ member.role }}</v-card-subtitle>
              <v-card-subtitle>
                <a class="text-black" :href="'mailto:' + member.email">
                  {{ member.email }}
                </a>
              </v-card-subtitle>
            </v-card>
          </v-col>
        </v-row>
      </v-card>
    </v-col>
    <v-col cols="12">
      <v-card class="text-center bg-transparent" flat
        ><v-card-title class="mt-4 mb-4">JRW History</v-card-title>
        <span>
          <a
            href="https://www.dropbox.com/scl/fi/7h2i1p57et9zxtxf3g25b/James-River-Women-s-Constitution-_-Revised-Feb-2021.pdf?rlkey=cr76b1gjd9bnfhmtkv8rrhpkd&e=1&dl=0"
            target="_blank"
            rel="noopener noreferrer"
            style="color: #092062"
          >
            CLICK HERE TO VIEW THE JRW CONSTITUTION
          </a> </span
        ><v-card-text
          >Stephanie H. Edwards (Stephie-Jo) formed James River Women’s Rugby
          Football Club (JWRFC) in the Spring of 2001. Before that, there was
          not a women’s club team in Richmond, VA. <br /><br />With the
          assistance of the James River Men’s and United Men’s RFC, JRWRFC was
          able to gather interested players from the area. Enough players came
          out to establish the need to schedule practices. With the enthusiasm
          of these new players, James River entered a team in the Cape Fear
          Sevens Tournament that summer.<br /><br />
          There was a positive reaction from the players to continue with a team
          in the fall. James River Men’s RFC, our established brother club,
          allowed us to use a portion of their field and assisted in coaching
          the new players during the fall season. <br /><br />
          Schedule practices began in mid-August and continued through the first
          part of November. Eight scheduled matches were played and several
          scrimmages with Virginia Commonwealth University Women’s Football Club
          were organized and executed. The team also participated in the Sandy
          Lee State Cup in late October. After a successful trial run, the women
          decided to move forward with the club.<br /><br />
          On January 15, 2002, the club held its inaugural Annual General
          Meeting (AGM). The club voted in Shannon Plum as the newly elected
          president; as well as, its first executive board. </v-card-text
        ><span class="text-h6 font-weight-bold"
          >Bleed Blue and Green!
        </span></v-card
      ></v-col
    >
  </div>
</template>

<script setup>
import Emily from "../assets/IMG_3397.jpeg";
import Trey from "../assets/IMG_3378.jpeg";
import Rachel from "../assets/IMG_3385.jpeg";
import Tylea from "../assets/IMG_3381.jpeg";
import Vicky from "../assets/IMG_9160.jpeg";
// Board Members Data
const boardMembers = ref([
  {
    name: "Emily Yanuskiewicz",
    role: "President",
    email: "president@jamesriverrugby.com",
    photo: Emily, // Path to the public folder
  },
  {
    name: "Jesse Pittard",
    role: "Vice President",
    email: "vp@jamesriverrugby.com",
    photo: "path/to/photo2.jpg",
  },
  {
    name: "Vicky Whydell",
    role: "Match Secretary",
    email: "matchsec@jamesriverrugby.com",
    photo: Vicky,
  },
  {
    name: "Grapes McElroy",
    role: "Treasurer",
    email: "finance@jamesriverrugby.com",
    photo: "path/to/photo4.jpg",
  },
  {
    name: "Trey Young",
    role: "Secretary",
    email: "teamsec@jamesriverrugby.com",
    photo: Trey,
  },
  {
    name: "Tylea Walker",
    role: "Recruitment Chair",
    email: "signup2play@jamesriverrugby.com",
    photo: Tylea,
  },
  {
    name: "Rachel McConaughy",
    role: "Social Chair",
    email: "socials@jamesriverrugby.com",
    photo: Rachel,
  },
  {
    name: "Tasha Conerly",
    role: "Diversity & Cultural Ambassador",
    email: "diversity@jamesriverrugby.com",
    photo: "path/to/photo9.jpg",
  },
  {
    name: "Shelby Morris",
    role: "Member at Large",
    email: "teamrep@jamesriverrugby.com",
    photo: "path/to/photo10.jpg",
  },
  {
    name: "Tim",
    role: "Head Coach",
    email: "teamrep@jamesriverrugby.com",
    photo: "path/to/photo10.jpg",
  },
]);
</script>

<style scoped>
/* Styling adjustments to ensure consistency */
.v-card-title,
.v-card-subtitle {
  padding: 0 10px;
  margin-bottom: 10px;
}

.v-img {
  border-radius: 50%; /* Make the image round */
  overflow: hidden;
}
</style>
