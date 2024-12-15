<template>
  <v-footer height="80" app class="logo">
    <v-row justify="center" no-gutters>
      <a
        v-for="item in items"
        :key="item.title"
        :href="item.href"
        :title="item.title"
        class="d-inline-block mx-2"
        rel="noopener noreferrer"
        target="_blank"
      >
        <v-icon :icon="item.icon" :size="30" color="blue-darken-4" />
      </a>

      <div
        class="text-disabled"
        style="position: absolute; right: 16px; margin-top: 6px"
      >
        <span class="text-blue-darken-4">
          &copy; 2001-{{ new Date().getFullYear() }}
        </span>

        <span class="d-none d-sm-inline-block text-blue-darken-4">
          by James River Women's Rugby</span
        >
      </div></v-row
    >
  </v-footer>
</template>

<script setup>
const items = [
  {
    title: "James River Women's Rugby Facebook",
    icon: "mdi-facebook",
    href: "https://www.facebook.com/JRWRFC/",
  },
  {
    title: "James River Women's Rugby Twitter",
    icon: "mdi-instagram",
    href: "https://www.instagram.com/jrwrugby/",
  },
  {
    title: "James River Women's Rugby Twitter",
    icon: [
      "M2.04875 3.00002L9.77052 13.3248L1.99998 21.7192H3.74882L10.5519 14.3697L16.0486 21.7192H22L13.8437 10.8137L21.0765 3.00002H19.3277L13.0624 9.76874L8.0001 3.00002H2.04875ZM4.62054 4.28821H7.35461L19.4278 20.4308H16.6937L4.62054 4.28821Z",
    ],
    href: "https://x.com/JRWRugby",
  },
];
</script>

<style scoped>
/* .social-link :deep(.v-icon) 
  color: rgba(var(--v-theme-on-background), var(--v-disabled-opacity))
  text-decoration: none
  transition: .2s ease-in-out

  &:hover
    color: #2E7D32 */

.logo {
  background-color: #243058;
}
</style>
