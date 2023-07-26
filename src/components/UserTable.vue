<script setup lang="ts">
import { ref } from "vue"

let users = ref<{ name: string; email: string }[]>([])
</script>

<template>
  <div class="d-flex justify-content-end">
    <button class="btn btn-primary">Add user</button>
  </div>
  <table class="table">
    <thead>
      <tr>
        <th>Name</th>
        <th>Email</th>
        <th>Actions</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="(user, index) in users" :key="index">
        <td>{{ user.name }}</td>
        <td>{{ user.email }}</td>
        <td>-</td>
      </tr>
    </tbody>
  </table>
</template>
