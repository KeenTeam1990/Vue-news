<template>
  <div>
    <my v-show="showMy"></my>
    <v-header class="pos-header"></v-header>
    <v-nav v-bind:msg="msg"></v-nav>
  </div>
</template>

<script>
import my from '@/components/my'
import vHeader from '@/components/vHeader'
import vNav from '@/components/vNav'

export default {

 data() {
    return{
      msg: [
         {src: require('../assets/qinliugan.jpg')},
         {src: require('../assets/huanqiu.jpg')},
         {src: require('../assets/aierlan.jpg')},
      ]
    }
  },

  created() {
    this.$store.commit('muShowMy', false)
  },
  components: {
    vHeader,
    vNav,
    my
  },
  computed: {
    showMy() {
      return this.$store.state.showMy
    }
  }
}
</script>

<style lang="css" scoped>
.pos-header {
  position: fixed;
  top: 0;
}
</style>
