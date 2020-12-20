<template>
  <v-main>
    <v-container fluid>
      <v-file-input
        v-model="image"
        chips
        multiple
        label="File input w/ chips"
      />
      <v-btn @click="uploadImage()">
        Upload
      </v-btn>
    </v-container>
  </v-main>
</template>

<script>

export default {

  components: {
  },
  data () {
    return {
      baseUrlUpload: 'https://api.imgbb.com/1/upload?key=51425d3514238597308f344f7f70ea50',
      image: null
    }
  },
  methods: {
    async uploadImage () {
      const response = await this.$axios.$post(this.baseUrlUpload, {
        headers: {
          'Content-Type': 'multipart/form-data'
        },
        body: {
          image: this.image
        }
      })
      console.log(response)
    }
  }
}
</script>
