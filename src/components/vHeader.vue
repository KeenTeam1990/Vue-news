<template lang="html">
  <div class="header">
    <img src="../assets/identify.png" @click="clickIcon">
    <span>爱新闻</span>
    <img src="../assets/search.png" @click="toSearch">
  </div>
</template>

<script>
export default {
  methods: {
    clickIcon() {
      this.$store.state.showMy = true
      this.$store.state.showLogin = true
    },

    toSearch() {
      this.$router.push('/search')
    },
  }
}
</script>

<style lang="css" scoped>
.header {
  width: 100%;
  height: 1.2rem;
  background-color: #888888;
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: #fff;
  font-size: 18px;
  font-weight: 600;
  letter-spacing: 2px;
  z-index: 99;

}
  img {
    width: .67rem;
    height: .67rem;
    padding: .4rem;
  }

</style>
