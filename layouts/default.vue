<template>
  <v-app dark>
    <Header :name="name" />
    <Nuxt /> <!--Renderização da página-->
    <Footer :name="name" />
  </v-app>
</template>

<script>
import Header from '~/components/core/Header'
import Footer from '~/components/core/Footer'

export default {
  components: {
    Header, Footer
  },
  data: () => ({
    name: 'Generic Site'
  })
}
</script>
