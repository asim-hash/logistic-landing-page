<template>
  <nav class="navbar is-dark has-shadow c-navbar-top" ref="c-navbar-top">
    <div class="container">
      <div class="navbar-brand">
        <a class="navbar-item" href="#main" v-smooth-scroll v-scroll-spy>
          <img :src="require('@/assets/images/logo.png')" alt="">
        </a>

        <div class="navbar-burger burger" :class="{ 'is-active': isNavbarOpen }" @click="toggleNavbar">
          <span></span>
          <span></span>
          <span></span>
        </div>
      </div>

      <div class="navbar-menu" :class="{ 'is-active': isNavbarOpen }">
        <div class="navbar-end">
          <a href="#about" class="navbar-item is-uppercase" v-smooth-scroll v-scroll-spy>О нас</a>
          <a href="#contact" class="navbar-item is-uppercase" v-smooth-scroll v-scroll-spy>Связатся</a>
          <a class="navbar-item">
            +996700999888
          </a>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
  export default {
    name: 'navbar-top',
    data () {
      return {
        lastKnownScrollPosition: 0,
        ticking: false,
        isNavbarOpen: false
      }
    },
    methods: {
      handleScroll () {
        const hasBackgroundClass = 'c-navbar-top--has-background'
        let navbarTop = this.$refs['c-navbar-top']

        if (process.browser) {
          if (window.scrollY > 100) {
            navbarTop.classList.add(hasBackgroundClass)
          } else {
            navbarTop.classList.remove(hasBackgroundClass)
          }
        }
      },
      toggleNavbar () {
        this.isNavbarOpen = !this.isNavbarOpen
      },
      throttleScrollHandling () {
        this.lastKnownScrollPosition = window.scrollY
        if (!this.ticking) {
          window.requestAnimationFrame(() => {
            this.handleScroll()
            this.ticking = false
          })
        }
        this.ticking = true
      }
    },
    created () {
      if (process.browser) {
        window.addEventListener('scroll', this.throttleScrollHandling)
      }
    },
    mounted () {
      this.handleScroll()
    },
    destroyed () {
      if (process.browser) {
        window.removeEventListener('scroll', this.throttleScrollHandling)
      }
    }
  }
</script>

<style lang="scss" scoped>
  @import "~bulma/sass/utilities/initial-variables";
  @import "~assets/scss/custom";

  .navbar {
    font-family: $family-secondary;

    &.is-dark {
      background-color: transparent;
    }
  }

  .c-navbar-top {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 5;
    transition: background .25s ease-in-out, margin .25s ease-in-out;
    margin: 1rem 0;
  }

  .c-navbar-top--has-background {
    margin: 0;

    &.is-dark {
      background-color: $black;
    }
  }

  /*.c-navbar-item--is-active {
    background: $darkred
  }*/
</style>
