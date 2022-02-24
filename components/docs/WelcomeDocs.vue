<template>
  <main class="site-main">
    <div class="content">
      <div class="header">
        <img src="~assets/img/aceslabs.png" alt="" />
        <h1>The Documentation</h1>
      </div>
      <p>
        It's still beta version, you can contribute build up at
        <a href="https://github.com/ghofaralhasyim/aces-base" target="blank">
          Github
        </a>
        .
      </p>
    </div>
  </main>
</template>
<script>
export default {
  name: 'WelcomeDocs'
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
