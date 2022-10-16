<script setup>
import { onMounted } from "vue"
import { RouterLink, RouterView } from "vue-router"
import HelloWorld from "./components/HelloWorld.vue"

const url = "https://masak-apa.tomorisakura.vercel.app"

const fetchFood = () => {
  fetch(`${url}/api/search/?q=coto`)
    .then((res) => console.log(res))
    // .then((data) => console.log(data))
    .catch((err) => console.log(err))
}
</script>

<template>
  <button @click="fetchFood">get food</button>
</template>
