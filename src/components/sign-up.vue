<template>
  <div>
    <div class="flex flex-col justify-center items-center h-screen">
      <img class="w-24 pb-4 mx-auto" src="../assets/logo.png" alt="logo" />
      <div>
        <input
          class="w-60 h-10 pl-5 block mb-7 mx-auto border-2 rounded-lg border-green-400"
          type="text"
          placeholder="Name"
          v-model="form.name"
        />
        <input
          class="w-60 h-10 pl-5 block mb-7 mx-auto border-2 rounded-lg border-green-400"
          type="text"
          placeholder="Email"
          v-model="form.email"
        />
        <input
          class="w-60 h-10 pl-5 block mb-7 mx-auto rounded-lg border-2 border-green-400"
          type="password"
          placeholder="Password"
          v-model="form.password"
        />
        <button
          class="w-full hover:bg-green-400 h-10 rounded-lg mb-7 mx-auto border-2 border-green-400"
          @click="submit"
        >
          Sign Up
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
import { reactive } from "vue";

const form = reactive({
  name: "",
  email: "",
  password: "",
});

const submit = () => {
  console.log("submit", form.email);
};
</script>
