<template>
  <div class="nav-bar flex items-center py4 text-xl justify-end px-8 box-border">
    <theme-switch class="mr"/>
    <div class="links flex items-center gap3">
      <div class="icon-btn i-carbon-logo-github"></div>
      <div class="icon-btn i-carbon-logo-twitter"></div>
      <div class="icon-btn i-carbon-logo-wechat"></div>
    </div>
  </div>
</template>

<script setup>
  import ThemeSwitch from './ThemeSwitch.vue'
  import { useDark, useToggle } from '@vueuse/core';
  const isDark = useDark()
  const toggleDark = useToggle(isDark)
</script>

<style scoped lang="scss">
.nav-bar{
  color: var(--text-light);
  border-bottom: 1px solid var(--nav-color);
  .links {
    .icon-btn{
      cursor: pointer;
      &:hover{
        color: var(--nav-icon-light);
      }
    }
    &::before{
      margin-right: 8px;
      margin-left: 8px;
      width: 1px;
      height: 24px;
      background-color: #CCC;
      content: "";
    }
  }
}
</style>