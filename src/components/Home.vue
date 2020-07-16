<template>
  <div class="home">
    <the-navbar />
    <search-field />
    <!-- <h2>Discover</h2> -->
    <listing-carousel />
    <recommended-mood />
  </div>
</template>

<script>
import TheNavbar from '@/components/TheNavbar.vue';
import SearchField from '@/components/SearchField.vue';
import ListingCarousel from '@/components/ListingCarousel.vue';
import RecommendedMood from '@/components/RecommendedMood.vue';

export default {
  name: 'Home',
  components: {
    TheNavbar,
    SearchField,
    ListingCarousel,
    RecommendedMood,
  },
};
</script>

<style lang="stylus" scoped>
.home {
  --homepage-padding-right: 11%;
  position: relative;
  z-index: 0;
  flex-grow: 1;
  width: 30%;
  min-height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-start;
  padding: 1em 4%;
  padding-right: 0;
  color: var(--text-color--primary);
  background: var(--bg-color--primary);

  /* apply padding-right to every direct descendant except Carousel */
  > *:not(.listing-carousel) {
    padding-right: var(--homepage-padding-right);
  }
}
</style>
