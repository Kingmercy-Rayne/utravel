<template>
  <ul class="listing-carousel__categories">
    <li>
      <h5 @click="setActiveCategory(1)" :class="activeCategory === 1 ? 'active_header' : ''">
        Experiences
      </h5>
    </li>
    <li>
      <h5 @click="setActiveCategory(2)" :class="activeCategory === 2 ? 'active_header' : ''">
        Places
      </h5>
    </li>
    <li>
      <h5 @click="setActiveCategory(3)" :class="activeCategory === 3 ? 'active_header' : ''">
        Housings
      </h5>
    </li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      categoryList: ['Experiences', 'Places', 'Housings'],
      activeCategory: 1,
    };
  },
  methods: {
    setActiveCategory(value) {
      this.activeCategory = value;
      this.$emit('categoryChange', value);
    },
  },
};
</script>
<style lang="stylus" scoped>
.listing-carousel__categories {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: flex-start;
  margin: 0.8em 0 1em;

  li {
    padding-right: 2em;

    h5 {
      font-weight: 500;
      cursor: pointer;
      transition: all 0.15s ease-in;
    }
  }
}

.active_header {
  position: relative;
  color: var(--text-color--tri);
  /* cheating with the !important tag */
  opacity: 1 !important;
  font-weight: 700 !important;

  /* dot marker */
  &:after {
    content: '';
    position: absolute;
    border: solid 0.15rem var(--text-color--tri);
    clip-path: circle(50% at 50% 50%);
    left: 48%;
    right: 48%;
    bottom: -1em;
    // height: 200px;
  }
}
</style>
