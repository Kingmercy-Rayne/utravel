<template>
  <div class="the__navbar">
    <div class="nav-toggle">
      <span class="hamburger"></span>
    </div>
    <button class="toggle">
      <span class="hamburger"></span>
    </button>
    <ul class="nav__list">
      <li><a href="">Discover</a></li>
      <li><a href="">Blog</a></li>
    </ul>
    <div class="profile">
      <img src="@/assets/img/cesar-rincon-XHVpWcr5grQ-unsplash.jpg" alt="" />
      <span></span>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="stylus" scoped>
.the__navbar {
  min-height: 20px;
  width: 100%;
  display: flex;
  align-items: center;

  .toggle {
    /* container class for hamburger */
    padding: 0.8em 0;
    background: none;
    border: none;
    text-align: center;
    /* TODO: determine why harmburger class aligns left and needs flexbox hack */
    display: flex;
    justify-content: center;
    align-items: center;

    .hamburger {
      display: block;
      position: relative;
      background: var(--text-color--primary);
      height: 0.16rem;
      width: 1.4rem;

      &::after {
        content: '';
        position: absolute;
        top: 7px;
        left: 0;
        height: 0.14rem;
        width: 0.9rem;
        background: var(--text-color--primary);
        transition: all 0.4s ease-in-out;
      }
    }
  }

  .nav__list {
    margin-left: auto;
    // border: solid thin yellow;
    display: flex;
    font-size: 0.8rem;
    font-weight: 700;

    li {
      padding: 0.5em 2em;
    }
  }

  .profile {
    position: relative;
    width: 2rem;
    height: 2rem;
    margin-left: 1em;
    cursor: pointer;

    img {
      border: solid thin #ccc;
      border-radius: 5px;
      clip-path: polygon(0 0, 70% 0, 100% 30%, 100% 99%, 0 100%, 0% 50%);
    }

    span {
      position: absolute;
      width: 7px;
      height: 7px;
      clip-path: circle(50% at 50% 50%);
      top: 0;
      right: 0;
      background: var(--text-color--tri);
    }
  }
}
</style>
