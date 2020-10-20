<template>
  <div>
    <navbar-top></navbar-top>

    <hero-index></hero-index>

    <projects-showcase></projects-showcase>

    <team></team>

    <contact></contact>

    <footer class="footer" style="background-color: hsl(0, 0%, 8%)">
      <div class="container has-text-grey">
        <div class="content has-text-centered">
          0700029541
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
  import NavbarTop from '~/components/NavbarTop.vue'
  import HeroIndex from '~/components/HeroIndex.vue'
  import ProjectsShowcase from '~/components/ProjectsShowcase.vue'
  import Team from '~/components/Team.vue'
  import Contact from '~/components/Contact.vue'

  export default {
    components: {
      NavbarTop,
      HeroIndex,
      ProjectsShowcase,
      Team,
      Contact
    }
  }
</script>
