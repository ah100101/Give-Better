<template>
    <nav
      class="navbar header has-shadow is-primary"
      role="navigation"
      aria-label="main navigation"
    >
      <div class="navbar-brand">
        <a
          class="navbar-item"
          href="/">
          <img
            src="~assets/buefy.png"
            alt="Buefy"
            height="28">
        </a>
        <a
          class="navbar-item"
          v-for='item in navItems'
          v-bind:key='item.url'
          v-html='item.title'
          v-on:click='sendTo(item.url)'/>
        <div class="navbar-burger">
          <span />
          <span />
          <span />
        </div>
      </div>
    </nav>
</template>

<script>
export default {
  data() {
    return {

    }
  },
  computed: {
    navItems: function () {
      return this.$store.getters['navigation/current']
    },
    showSignOut: function () {
      return this.$store.getters['navigation/showSignOut']
    }
  }
}
</script>
