<template>
  <div>
    <h2 class="vue-cli__title">Vue cli App</h2>

    <nav>
      <router-link to="/vue-cli/">Home</router-link> |
      <router-link to="/vue-cli/about">About</router-link>
    </nav>
  </div>
  <router-view />
</template>

<script setup>
import { onMounted } from "vue";

onMounted(() => {
  const rootElement = document.getElementById(
    "single-spa-application:@micro/vue-cli"
  );
  rootElement.classList.add("vue-cli");
});
</script>

<style lang="scss">
nav {
  a {
    font-weight: bold;
    color: #1d2a39;

    &.router-link-exact-active {
      color: #195365;
    }
  }
}

.vue-cli {
  background: #42b983;
  border: 2px solid #278359;

  &__title {
    font-size: 50px;
    color: #424d57;
  }
}
</style>
