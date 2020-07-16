<template>
  <section class="promo__container">
    <div class="backdrop__img">
      <img src="@/assets/img/soma-laszlo-zTV097FMWyw-unsplash.jpg" alt="" />
      <!-- <img src="@/assets/img/anders-jilden-AkUR27wtaxs-unsplash.jpg" alt="" /> -->
      <!-- <img src="@/assets/img/aranprime-IRpVarAfRyg-unsplash.jpg" alt="" /> -->
    </div>
    <div class="foreword__container">
      <h1 class="foreword">Get ready for your lifetime journey!</h1>
      <h4>
        Collection of the most beautiful places, experiences and unusual housings in the world
      </h4>
      <button class="cta__btn">Get Started</button>
    </div>
  </section>
</template>

<script>
export default {
  name: 'PromoContainer',
};
</script>

<style lang="stylus" scoped>
// border-radius =
// local variable that controls radius value for top/bottom-right
.promo__container {
  --border-radius: 2em;
  position: relative;
  z-index: 10;
  width: 60%;
  flex-grow: 1;
  display: flex;
  justify-content: flex-start;
  align-items: center;
  padding-left: 8%;
  color: var(--text-color--alt);
  border-top-right-radius: var(--border-radius);
  border-bottom-right-radius: var(--border-radius);
  box-shadow: 2px 4px 8px 0px rgba(0, 0, 0, 0.5);

  .backdrop__img {
    position: absolute;
    left: 0;
    top: 0;
    right: 0;
    bottom: 0;
    z-index: -10;
    filter: brightness(55%);

    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      object-position: center right;
      border-top-right-radius: var(--border-radius);
      border-bottom-right-radius: var(--border-radius);
    }
  }

  .foreword__container {
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: flex-start;
    margin-bottom: 2em;
    text-align: left;

    .foreword {
      width: 70%;
      // margin-top: 2em;
      font-weight: 500;
      font-size: 2.8rem;
    }

    h4 {
      width: 80%;
      margin: 1em 0;
      font-weight: 400;
      font-size: 1rem;
    }

    .cta__btn {
      margin-top: 1.5em;
      background: var(--button-bg--primary);
      border: none;
    }
  }
}
</style>
