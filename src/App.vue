<script setup lang="ts">
import NavBar from "./components/NavBar.vue"
import UserTable from "./components/UserTable.vue"
</script>

<template>
  <NavBar msg="Vite + Vue" />
  <div class="container p-4">
    <UserTable />
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
