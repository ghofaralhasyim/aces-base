<template>
  <main class="site-main">
    <div class="content">
      <div class="header">
        <img src="~assets/img/aceslabs.png" alt="" />
        <h1>ACES Labs</h1>
      </div>
      <div>
        <h5>Welcome to ACES Base Code</h5>
        <p>
          It's based on Nuxt JS, we recommend you take a look at the
          <a href="https://nuxtjs.org/" target="blank"> Nuxt documentation </a>
          and <nuxt-link to="/documentation"> ACES Documentation </nuxt-link>,
          wether you are new or have previous experience with the framework.
        </p>
      </div>
    </div>
  </main>
</template>
<script>
export default {
  name: 'WelcomePage'
}
</script>
<style lang="scss" scoped>
.site-main {
  width: 100%;
  background-color: #fafafa;
  display: flex;
  justify-content: center;
  height: 100vh;
}

.content {
  width: 93%;
  padding: 70px 0 6em 0;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;

  @media #{$large} {
    padding-top: 100px;
    padding-left: 320px;
    padding-right: 320px;
  }
}

.header {
  display: flex;
  align-items: center;
}

.label {
  padding: 2px 8px;
  border-radius: 5px;
  background-color: rgb(226, 233, 238);
  color: #3b3b3b;
  font-size: 0.9em;
}
</style>
