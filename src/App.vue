<template>
  <div id="app">
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div> -->
    <Header />
    <div class="container">
      <router-view/>
    </div>
  </div>
</template>

<script>
import Header from '@/components/Header'

export default {
  components: {
    Header
  }
}

</script>


<style lang="scss">

</style>
