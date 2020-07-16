<template>
  <div id="app">
    <promo-container />
    <home />
  </div>
</template>

<script>
import PromoContainer from '@/components/PromoContainer.vue';
import Home from '@/components/Home.vue';

export default {
  name: 'App',
  components: {
    PromoContainer,
    Home,
  },
};
</script>

<style lang="scss">
#app {
  width: 100%;
  min-height: 100vh;
  font-family: var(--font-family--primary);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background: #fff;
  // border: solid thin black;
  display: flex;
}
</style>
