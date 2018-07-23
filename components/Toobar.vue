<template>
  <v-toolbar dark color="blue">
    <v-toolbar-side-icon></v-toolbar-side-icon>

    <v-toolbar-title class="white--text">
        <nuxt-link class="title" to="/">Devda</nuxt-link>
    </v-toolbar-title>

    <v-spacer></v-spacer>

    <v-btn icon>
      <v-icon>search</v-icon>
    </v-btn>

    <v-btn icon>
      <v-icon>refresh</v-icon>
    </v-btn>

  </v-toolbar>
</template>

<style scoped>
.title {
    text-decoration: none !important;
}
.title:visited {
    color: white;
}
</style>
