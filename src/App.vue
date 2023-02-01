<script setup lang="ts">
import { isMobileOrPc } from "./utils/utils";
import home from './views/home.vue'
// import { RouterLink, RouterView } from 'vue-router'

if (isMobileOrPc()) {
  var width = window.screen.width;
  window.document.getElementsByTagName("html")[0].style.fontSize =
    width / 7.5 + "px";
}
</script>

<template>
<home />
</template>

<style scoped>
.nav {
  z-index: 20;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
}
</style>
