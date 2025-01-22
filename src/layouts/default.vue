<template>
  <v-app>
    <Navigation></Navigation>
    <v-main class="d-flex flex-column" style="background-color: #029345">
      <router-view />
    </v-main>
    <AppFooter class="mt-auto" />
  </v-app>
</template>
