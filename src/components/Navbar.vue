<template>
  <nav>
    <router-link to="/">Home</router-link>
    <router-link to="/about">About</router-link>
    <router-link to="/projects">Projects</router-link>
  </nav>
</template>

<style>
nav {
  display: flex;
  gap: 20px;
  padding: 20px;
}

.router-link-active {
  color: blue;
  font-weight: bold;
}
</style>