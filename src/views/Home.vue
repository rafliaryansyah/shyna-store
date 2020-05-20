<template>
  <div class="home">
    <HeaderVyna />
    <HeroVyna />
    <BannerVyna />
    <InstaVyna />
    <PartnerVyna />
    <FooterVyna />
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import HeaderVyna from '@/components/HeaderVyna.vue';
import HeroVyna from '@/components/HeroVyna.vue';
import BannerVyna from '@/components/BannerVyna.vue';
import InstaVyna from '@/components/InstaVyna.vue';
import PartnerVyna from '@/components/PartnerVyna.vue';
import FooterVyna from '@/components/FooterVyna.vue';

export default {
  name: 'Home',
  components: {
    HeaderVyna,
    HeroVyna,
    BannerVyna,
    InstaVyna,
    PartnerVyna,
    FooterVyna
  }
};
</script>
