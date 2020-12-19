<template>
  <v-footer app>
    <span>All Rights Reserved {{ name }} {{ date }}</span>
    <slot />
    <slot name="test" />
  </v-footer>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      required: true
    }
  },
  data: () => ({
    date: new Date().getFullYear()
  })
}
</script>
