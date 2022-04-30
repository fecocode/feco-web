<script setup lang="ts">
import Logo from '../components/Logo.vue';
import SocialNetworks from '../components/SocialNetworks.vue';
</script>

<template>
  <div class="home">
    <Logo />
    <SocialNetworks />
  </div>
</template>

<style lang="scss" scoped>
.home {
  display: flex;
  flex-direction: column;
  gap: 105px;
}
</style>
