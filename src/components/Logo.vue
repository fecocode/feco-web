<script setup lang="ts">
import LogoSvg from '../assets/feco-logo.svg'
</script>

<template>
  <div class="logo">
    <img :src="LogoSvg" class="image" />
  </div>
</template>

<style lang="scss" scoped>
.logo {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: fit-content;
  animation: logo-fade-in 1s forwards ease-in;

  .image {
    width: 214px;
    user-select: none;
  }
}

@keyframes logo-fade-in {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
</style>
