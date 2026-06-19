<script setup>
import { useRoute } from "vue-router";

const route = useRoute();

const projects = [
  {
    id: 1,
    title: "Portfolio Website",
    description: "Created using Vue.js",
  },
  {
    id: 2,
    title: "Blog Website",
    description: "Created using Vue Router",
  },
  {
    id: 3,
    title: "Todo App",
    description: "Created using Vue Composition API",
  },
];

const project = projects.find(
  (item) => item.id == route.params.id
);
</script>

<template>
  <div>
    <h1>Project Detail</h1>

    <div v-if="project">
      <h2>{{ project.title }}</h2>
      <p>{{ project.description }}</p>
    </div>

    <div v-else>
      <p>Project not found.</p>
    </div>
  </div>
</template>