<template>
  <div class="recommended-mood">
    <div class="mood__header">
      <h4>Adventurous Mood?</h4>
      <h6>Show all</h6>
    </div>
    <recommended-mood-items />
  </div>
</template>

<script>
import RecommendedMoodItems from '@/components/RecommendedMoodItems.vue';

export default {
  name: 'RecommendedMood',
  components: {
    RecommendedMoodItems,
  },
};
</script>
<style lang="stylus" scoped>
.recommended-mood {
  width: 100%;
  min-height: 10vh;
  margin: 2em 0;

  .mood__header {
    display: flex;
    justify-content: space-between;
    align-items: center;

    h4 {
      // cursor: pointer;
    }

    h6 {
      opacity: 0.8;
      cursor: pointer;
    }
  }
}
</style>
