<script setup lang="ts">
import InstagramSvg from '../assets/feco-instagram.svg'
import GitHubSvg from '../assets/feco-github.svg'
import TwitterSvg from '../assets/feco-twitter.svg'

const links = {
  twitter: 'https://twitter.com/fecocode',
  github: 'https://github.com/fecocode/',
  instagram: 'https://www.instagram.com/fecocode/',
}

function goTo(link: 'twitter' | 'github' | 'instagram'): void {
  window.open(links[link], '_blank')
}

</script>

<template>
  <div class="social-networks">
    <img :src="TwitterSvg" class="icon" @click="goTo('twitter')" />
    <img :src="GitHubSvg" class="icon" @click="goTo('github')" />
    <img :src="InstagramSvg" class="icon" @click="goTo('instagram')" />
  </div>
</template>

<style lang="scss" scoped>
.social-networks {
  display: flex;
  gap: 40px;

  @for $i from 1 through 3 {
    .icon:nth-child(#{$i}n) {
      animation-delay:  #{$i * 0.25 + 1}s;
    }
  }
  .icon {
    height: 48px;
    cursor: pointer;
    user-select: none;
    transition: 500ms;
    border-radius: 100%;
    animation: fade-in 500ms forwards ease-in;
    opacity: 0;
    &:hover {
      box-shadow: 0px 0px 15px -2px #eee;
    }
  }
}

@keyframes fade-in {
  0% {
    opacity: 0;
    transform: translateY(-10px)
  }
  100% {
    opacity: 1;
    transform: translateY(0)
  }
}
</style>
