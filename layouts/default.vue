<template>
  <v-app dark>
    <Header :name="name" @doThing="updateSomething()" />
    <Nuxt /> <!--Renderização da página-->
    <Footer :name="name">
      <span> Sloted content</span>
    </Footer>
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
  }),
  methods: {
    updateSomething () {
      console.log('emmit works')
    }
  }
}
</script>
