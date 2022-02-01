<template>
    <v-container>
    <h2 class="text-center">Gallery</h2>
      <v-row>
        <v-col v-for="(item, i) in items" :key="i" class="d-flex child-flex" cols="6" sm="4">
          <v-card flat tile class="d-flex">
            <v-img :src="item.src" aspect-ratio="1" class="grey lighten-2">
              <template v-slot:placeholder>
                <v-row class="fill-height ma-0" align="center" justify="center">
                  <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
                </v-row>
              </template>
            </v-img>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
</template>

<script>

const items = [
    {
        src: require('./../static/images/full.jpg')
    },
    {
        src: require('./../static/images/full_2.jpg')
    },
    {
        src: require('./../static/images/preview.jpg')
    },
    {
        src: require('./../static/images/full_2.jpg')
    },
    {
        src: require('./../static/images/full_2.jpg')
    },
    {
        src: require('./../static/images/preview_2.jpg')
    },
    {
        src: require('./../static/images/full.jpg')
    },
]

export default {
  name: "News",
  data() {
    return {
      items,
    };
  },
};
</script>