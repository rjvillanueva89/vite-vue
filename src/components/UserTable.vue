<script setup lang="ts">
import { ref } from "vue"

let users = ref<{ name: string; email: string }[]>([])
let name = ref()
let email = ref()

function addUser() {
  users.value.push({ name: name.value, email: email.value })
  name.value = ""
  email.value = ""
}
</script>

<template>
  <div class="row">
    <div class="col">
      <h2>Users</h2>
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
    </div>
    <div class="col">
      <h2>New User</h2>
      <form>
        <div class="mb-3">
          <label for="name" class="form-label">Name:</label>
          <input type="text" class="form-control" id="name" v-model="name" />
        </div>
        <div class="mb-3">
          <label for="email" class="form-label">Email address:</label>
          <input type="email" class="form-control" id="email" v-model="email" />
        </div>
      </form>
      <div class="d-flex justify-content-end">
        <button class="btn btn-primary" @click="addUser()">Add</button>
      </div>
    </div>
  </div>
</template>
