<template>
  <div id="app" class="sticky-container">
    <div class="sticky-container-item">
      <Header />
    </div>
    <div class="sticky-container-item --push">
      <nuxt />
    </div>
  </div>
</template>

<script>
export default {
  name: 'DefaultLayout'
}
</script>

<style lang="scss" scoped></style>
