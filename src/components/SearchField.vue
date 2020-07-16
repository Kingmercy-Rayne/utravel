<template>
  <div class="search__field" :class="isInputActive == 1 ? 'input-active' : ''">
    <i class="fas fa fa-search"></i>
    <input
      type="search"
      name="Search"
      placeholder="Search"
      id="search__input"
      @focus="isInputActive = true"
      @blur="isInputActive = false"
      @
    />
  </div>
</template>

<script>
export default {
  data() {
    return {
      isInputActive: false,
    };
  },
};
</script>
<style lang="stylus" scoped>
.search__field {
  // padding: 0;
  position: relative;
  width: 80%;
  min-height: 20px;
  align-self: flex-start;
  display: flex;
  justify-content: flex-start;
  padding: 0.4em 0;
  margin: 1.5em 0;
  // margin-right: var(--homepage-padding-right);
  border: none;
  border-bottom: solid thin var(--border-color--primary);

  i {
    font-size: 1rem;
    transition: all 0.2s ease-in-out;
    cursor: pointer;

    &:hover {
      transform: scale(1.05);
    }
  }

  input[type='search'] {
    width: 100%;
    margin: 0 0.5em;
    padding: 0 0 0.5em 1em;
    font-size: 0.9rem;
    border: none;

    &:focus {
      outline: none;
    }
  }
}

.input-active {
  box-shadow: 0 8px 5px -5px rgba(81, 203, 238, 0.7);
}
</style>
