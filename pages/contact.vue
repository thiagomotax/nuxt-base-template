<template>
  <v-main>
    <v-container fluid>
      <input type="file" @change="onFileSelected">
      <v-btn @click="onUpload">
        upload
      </v-btn>
      <!-- <v-btn @click="uploadImage()">
        Upload
      </v-btn> -->
    </v-container>
  </v-main>
</template>

<script>

export default {

  components: {
  },
  data () {
    return {
      baseUrlUpload: 'https://api.imgbb.com/1/upload?key=810df06b0e99728c490dc897607f39ca',
      selectedFile: null
    }
  },
  methods: {
    onFileSelected (event) {
      this.selectedFile = event.target.files[0]
    },
    async onUpload () {
      const image = new FormData()
      image.append('image', this.selectedFile)
      const response = await this.$axios.$post('/api?key=810df06b0e99728c490dc897607f39ca',
        image
      )
      console.log(response)
    }
  }
}
</script>
