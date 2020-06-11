<template>
  <nav class="navbar is-dark" role="navigation" aria-label="main navigation">
    <div class="navbar-brand">
      <div class="navbar-item">Test</div>
      <div class="navbar-burger" data-target="navMenu" @click="$store.commit('toggleMenu')" :class="{'is-active': $store.state.isMenuActive}">
        <span></span>
        <span></span>
        <span></span>
      </div>
    </div><!-- navbar-brand END -->
    <div class="navbar-menu" id="navMenu" :class="{'is-active': $store.state.isMenuActive}">
      <div class="navbar-end">
        <nuxt-link to="/" class="navbar-item">Top</nuxt-link>
        <nuxt-link to="/about" class="navbar-item">About</nuxt-link>
        <nuxt-link to="/contact" class="navbar-item">Contact</nuxt-link>
      </div>
    </div><!-- navbar-menu END -->
  </nav>
</template>

<script>
export default {
  data: () => {
    return {isMenuActive: false}
  },
  methods: {
    toggleMenu () {
      this.isMenuActive = !this.isMenuActive
    }
  }
}
</script>