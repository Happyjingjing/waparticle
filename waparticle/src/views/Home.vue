<template>
  <div class="home">
    <share />
    <home-top />
    <home-article />

  </div>
</template>

<script>

import share from '@/components/homePage/share'
import homeTop from '@/components/homePage/homeTop'
import homeArticle from '@/components/homePage/homeArticle'

export default {
  name: 'home',
  components: {
    share,
    homeTop,
    homeArticle
  },
  data () {
    return {

    }
  },

}
</script>

<style>
.purple {
  background: #363557;
}
</style>

