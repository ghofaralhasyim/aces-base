<template>
  <div>
    <div class="sidebar" :class="{ active: toggle }">
      <ul class="nav-item">
        <nuxt-link v-for="data in dataNav" :key="data.title" :to="data.url"
          ><li class="nav-link">{{ data.title }}</li></nuxt-link
        >
      </ul>
    </div>
    <div
      class="overlay"
      :class="{ 'overlay-active': !toggle }"
      @click="toggler"
    ></div>
  </div>
</template>

<script>
export default {
  name: 'SideNav',
  props: {
    toggle: {
      type: Boolean,
      default: false
    },
    dataNav: {
      type: Array,
      default: () => []
    }
  },
  methods: {
    toggler() {
      this.$emit('toggle-overlay')
    }
  }
}
</script>

<style lang="scss" scoped>
.sidebar {
  position: fixed;
  top: 60px;
  left: 0;
  width: 200px;
  background-color: #fff;
  height: 100vh;
  z-index: 4;
  border-right: 1px solid rgba($color: #000000, $alpha: 0.1);
  transform: translateX(-100%);
  transition: 0.5s ease;

  @media #{$large} {
    transform: translateX(0);
  }
}

.active {
  transform: translateX(0);
}

.overlay {
  position: fixed;
  top: 0;
  left: 0;
  background-color: rgba($color: #000000, $alpha: 0.2);
  width: 100%;
  height: 100%;
  z-index: 3;
  opacity: 1;
  transition: overlaynimation 0.5s ease;
}

.overlay-active {
  display: none;
}

.nav-item {
  padding: 0;
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
  letter-spacing: 0.5px;
  color: #5c5c5c;

  a {
    text-decoration: none;
    color: #5c5c5c;
  }

  .nuxt-link-active {
    color: #5c5c5c;
  }

  .nav-link {
    list-style: none;
    padding: 1.5em 2em;
    border-bottom: 1px solid rgba($color: #000000, $alpha: 0.1);
  }
}
</style>
