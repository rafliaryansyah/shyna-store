<template>
  <div class="home">
    <HeaderVyna />
    <HeroVyna />
    <BannerVyna /> 
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import HeaderVyna from '@/components/HeaderVyna.vue';
import HeroVyna from '@/components/HeroVyna.vue';
import BannerVyna from '@/components/BannerVyna.vue';

export default {
  name: 'Home',
  components: {
    HeaderVyna,
    HeroVyna,
    BannerVyna
  }
};
</script>
