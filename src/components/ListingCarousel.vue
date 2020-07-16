<template>
  <div class="listing-carousel">
    <h2>Discover</h2>
    <Listing-carousel-categories @categoryChange="changeCarouselData" />
    <Listing-carousel-items :img_list="active_list" />
  </div>
</template>

<script>
import ListingCarouselCategories from '@/components/ListingCarouselCategories.vue';
import ListingCarouselItems from '@/components/ListingCarouselItems.vue';

export default {
  components: {
    ListingCarouselCategories,
    ListingCarouselItems,
  },
  data() {
    return {
      experiences_img_list: [
        'josh-soriano-XjDuNQr972w-unsplash',
        'nicolas-hans-0HFkStS9Gq0-unsplash',
        'jc3211-BpEH3K1G520-unsplash',
      ],
      places_img_list: [
        'ben-klea-C9Y3uijIrbc-unsplash',
        'jean-vella-AMUXeE7Y2Vc-unsplash',
        'james-donovan-lTxlm6e67XI-unsplash',
      ],
      housings_img_list: [
        'jc3211-BpEH3K1G520-unsplash',
        'roland-losslein-DmDYX_ltI48-unsplash',
        'jean-vella-AMUXeE7Y2Vc-unsplash',
      ],
      // set a default/ initial list for active_list
      active_list: [
        'josh-soriano-XjDuNQr972w-unsplash',
        'nicolas-hans-0HFkStS9Gq0-unsplash',
        'jc3211-BpEH3K1G520-unsplash',
      ],
    };
  },
  methods: {
    changeCarouselData(value) {
      // empty list before repopulating to combat lag in image load
      this.active_list = [];
      // switch the list(active_list) that gets passed into the carousel prop
      if (value === 3) {
        this.active_list = this.housings_img_list;
      } else if (value === 2) {
        this.active_list = this.places_img_list;
      } else {
        this.active_list = this.experiences_img_list;
      }
    },
  },
};
</script>
<style lang="stylus" scoped>
.listing-carousel {
  width: 100%;
  min-height: 200px;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: flex-start;
}
</style>
