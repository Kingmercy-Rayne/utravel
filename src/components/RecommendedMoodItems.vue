<template>
  <ul class="recommended-mood-items">
    <li class="mood__item">
      <div class="mood__item__art">
        <img src="@/assets/svg/kayak.svg" alt="" />
      </div>
      <h6 class="mood__item__text">Kayaking</h6>
    </li>
    <li class="mood__item">
      <div class="mood__item__art">
        <img src="@/assets/svg/discover.svg" alt="" />
      </div>
      <h6 class="mood__item__text">Ballooning</h6>
    </li>
    <li class="mood__item">
      <div class="mood__item__art">
        <img src="@/assets/svg/mountain.svg" alt="" />
      </div>
      <h6 class="mood__item__text">Hiking</h6>
    </li>
    <li class="mood__item">
      <div class="mood__item__art">
        <img src="@/assets/svg/snowboard.svg" alt="" />
      </div>
      <h6 class="mood__item__text">Snowboarding</h6>
    </li>
    <li class="mood__item">
      <div class="mood__item__art">
        <img src="@/assets/svg/safari.svg" alt="" />
      </div>
      <h6 class="mood__item__text">Safari</h6>
    </li>
  </ul>
</template>

<script>
export default {};
</script>
<style lang="stylus" scoped>
.recommended-mood-items {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0.5em 0 0 0.5em;

  .mood__item {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    margin: 0.5em 0;

    // border: solid thin brown;
    .mood__item__art {
      position: relative;
      z-index: 1;
      padding: 0.3em;
      background: #ddd;
      box-shadow: 0 8px 8px 0 rgba(0, 0, 0, 0.1);

      img {
        position: relative;
        z-index: -5;
        width: 2.2rem;
        height: 2rem;
        object-fit: cover;
      }
    }

    .mood__item__text {
      padding: 0.5em 0;
      opacity: 0.8;
    }
  }
}
</style>
