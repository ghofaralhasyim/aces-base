<template>
  <div>
    <header class="header">
      <div class="grid container">
        <div class="grid_column" col="s6,m2">
          <div class="nav-brand font--bold">
            <img
              src="~static/img/menu-bar.svg"
              class="toggler"
              alt=""
              @click="toggle"
            />
            <nuxt-link to="/">
              <img src="~assets/img/aceslabs.png" class="site-logo" alt="" />
              <i>ACES Labs</i>
            </nuxt-link>
          </div>
        </div>
        <nav class="grid_column main-nav" col="s6,m10">
          <a href="https://github.com/ghofaralhasyim/aces-base" target="blank"
            ><img src="~static/img/github.svg" alt=""
          /></a>
        </nav>
      </div>
    </header>
    <headerSidenav
      :toggle="toggler"
      :data-nav="sideNav"
      @toggle-overlay="toggle"
    />
  </div>
</template>

<script>
export default {
  name: 'HeaderComp',
  data() {
    return {
      toggler: false,
      sideNav: [
        {
          title: 'Getting Started',
          url: '/documentation'
        },
        {
          title: 'Typography',
          url: '/documentation/typography'
        }
      ]
    }
  },
  methods: {
    toggle() {
      this.toggler = !this.toggler
    }
  }
}
</script>
<style lang="scss" scoped>
.header {
  display: flex;
  position: fixed;
  z-index: 5;
  top: 0;
  left: 0;
  width: 100%;
  background-color: #142133;
  height: 60px;
  box-shadow: 0px 5px 8px rgba(#000, 0.2);
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  color: #fff;

  @media #{$md} {
    height: 60px;
  }
}

.container {
  width: 100%;
  max-width: 100%;
  padding: 0 2em;
}

.nav-brand {
  font-size: 1.25em;
  display: flex;
  align-items: center;
  .site-logo {
    width: 100%;
    max-width: 30px;
  }

  .toggler {
    width: 1.25em;
    margin-right: 1em;
    @media #{$large} {
      display: none;
    }
  }
}

.main-nav {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  color: #fff;
}

a {
  text-decoration: none;
  color: #fff;
  padding: 0;
  margin: 0;
  display: flex;
  align-items: center;
}
</style>
