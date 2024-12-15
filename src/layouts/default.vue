<template>
  <v-app>
    <template>
      <div class="text-center pa-4">
        <v-dialog v-model="dialog" width="auto">
          <v-card
            class="text-center bg-green-darken-3"
            max-width="450"
            min-height="100"
            rounded="xl"
          >
            <v-card-title class="text-h6">
              Welcome To The Home Of <br />
              James River Women's Rugby Football Club
            </v-card-title>
            <v-card-text class="text-subtitle-1 mt-n3">
              No experience necessary! </v-card-text
            ><v-img :src="crest" max-height="200"></v-img>
            <template v-slot:actions>
              <v-icon
                size="x-large"
                class="mr-2"
                icon="mdi-rugby"
                @click="dialog = false"
              ></v-icon>
            </template>
          </v-card>
        </v-dialog>
      </div>
    </template>
    <Navigation></Navigation>
    <v-main class="bg-white">
      <router-view />
    </v-main>
    <AppFooter />
  </v-app>
</template>

<script setup>
import crest from "../assets/JRWRFC_Crest.png";
const dialog = ref(false);

onMounted(() => {
  dialog.value = true;
});
</script>
