<template>
    <div>
      <v-container
        fluid
        grid-list-lg
      >
        <v-layout row wrap>

          <v-flex xs12>
            <v-card :color="color" class="white--text" :href="url">
              <v-layout>
                <v-flex xs5>
                  <v-card-media
                    :src="image"
                    height="100px"
                    contain
                  ></v-card-media>
                </v-flex>
                <v-flex xs7>
                  <v-card-title primary-title>
                    <div>
                      <div class="headline">{{ title }}</div>
                      <div>{{ artistName }}</div>
                    </div>
                  </v-card-title>
                </v-flex>
              </v-layout>
              <v-divider light></v-divider>
              <v-card-actions class="pa-3">
                Rate this album
                <v-spacer></v-spacer>
                <v-icon>star_border</v-icon>
                <v-icon>star_border</v-icon>
                <v-icon>star_border</v-icon>
                <v-icon>star_border</v-icon>
                <v-icon>star_border</v-icon>
              </v-card-actions>
            </v-card>
          </v-flex>

        </v-layout>
      </v-container>
    </div>
</template>

<script>
export default {
    props: ['title', 'image', 'artistName', 'url', 'color']
}
</script>
