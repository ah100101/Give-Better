<template>
  <div v-cloak>
    <TopNav />
    <section class="main-content">
        <nuxt />
    </section>
  </div>
</template>

<script>
import TopNav from '~/components/TopNav.vue'

export default {
  data() {
    return {

    }
  },
  components: {
    TopNav
  }
}
</script>
