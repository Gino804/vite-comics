<script>

import AppHeader from './components/AppHeader.vue';

export default {
  components: {
    AppHeader
  }
}
</script>

<template>
  <AppHeader />
</template>

<style>
/* CSS Reset */

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* Generics */

body {
  font-family: "Open Sans", sans-serif;
}

ul {
  list-style-type: none;
}

a {
  text-decoration: none;
}

/* Utils */

.container {
  max-width: 1200px;
  margin: 0 auto;
}
</style>