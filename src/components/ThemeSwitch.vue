<template>
  <div class="theme-switch flex items-center dark:justify-end" @click="toggleDark()">
    <div class="icon-wrap flex-center" v-if="!isDark">
      <div class="i-carbon-sun w-12px h-12px"></div>
    </div>
    <div class="icon-wrap flex-center" v-else>
      <div class="i-carbon-moon w-12px h-12px"></div>
    </div>
  </div>
</template>

<script setup>
import { useDark, useToggle } from '@vueuse/core';
  const isDark = useDark()
  const toggleDark = useToggle(isDark)
</script>

<style scoped lang="scss">
.theme-switch {
  position: relative;
  border-radius: 12px;
  width: 40px;
  height: 22px;
  border: 1px solid var(--switch-boder-color);
  background-color: var(--switch-bg);
  cursor: pointer;
  &:hover{
    border-color: var(--switch-hover-border);
  }
  .icon-wrap {
    width: 18px;
    height: 18px;
    background: var(--bg-color);
    border-radius: 50%;
  }
}
</style>