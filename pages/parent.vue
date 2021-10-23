<template>
  <div>
    <h1>Parent</h1>
    <ul class="flex">
      <li v-for="(link, index) in links" :key="index">
        <NuxtLink class="mr-2" :to="link.url">{{ link.name }}</NuxtLink>
      </li>
    </ul>
    <NuxtChild />
  </div>
</template>

<script setup lang="ts">
import {reactive} from "vue"

const links: any = reactive([
    {name: "Parent", url: "/parent"},
    {name: "Child", url: "/parent/child"},
    {name: "Test", url: "/parent/test"},
  ])
</script>
