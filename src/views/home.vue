<script setup lang="ts">
import NavBar from '../components/NavBar.vue'
import Article from '../components/Article.vue'

</script>
<template>
  <header class="nav">
    <nav-bar />
  </header>
  <main>
    <div class="main-left">
      <Article></Article>
    </div>
  </main>
</template>

<style lang="scss" scoped>
.main-left {
  width: 700px;
}
</style>