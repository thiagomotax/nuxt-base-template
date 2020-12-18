<template>
  <div>
    <v-navigation-drawer v-model="drawer" absolute temporary app>
      <v-list
        nav
        dense
      >
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-home</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Home</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-account</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Account</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar app color="deep-purple">
      <v-app-bar-nav-icon @click="drawer = true">
        <!--  -->
      </v-app-bar-nav-icon>
      <v-toolbar-title>{{ name }}</v-toolbar-title>
    </v-app-bar>
  </div>
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
    drawer: false,
    group: null
  })
}
</script>
