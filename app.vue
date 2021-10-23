<template>
  <div>
    <ul class="flex">
      <li v-for="(link, index) in links" :key="index">
        <NuxtLink class="mr-2" :to="link.url">{{ link.name }}</NuxtLink>
      </li>
    </ul>
    <NuxtPage />
  </div>
</template>

<script setup lang="ts">
import {reactive} from "vue"

const links: any = reactive([
    {name: "Home", url: "/"},
    {name: "About", url: "/about"},
    {name: "Blog", url: "/blog"},
    {name: "Parent", url: "/parent"},
  ])
</script>

<style>
.flex {
  display: flex;
}
.mr-2 {
  margin-right: 2rem;
}
</style>