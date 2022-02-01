<template>
  <v-carousel
    cycle
    height="400"
    hide-delimiter-background
    show-arrows-on-hover
  >
    <v-carousel-item
      v-for="(article, i) in slides"
      :key="i"
    > 
      <v-sheet
        :color="colors[1]"
        height="100%"
        v-if="article.slider"
      >
        <v-row
          class="fill-height"
          align="center"
          justify="center"
        >
          <div class="text-h4">
            {{ article.name }}
          </div>
        </v-row>
      </v-sheet>
    </v-carousel-item>
  </v-carousel>
</template>

<script>
import Vue from 'vue';
import news from '../static/articles.json';
import Vuetify from "vuetify/lib";
import "vuetify/dist/vuetify.min.css";

Vue.use(Vuetify)
  const slides = news.filter(item => item.slider === true);

  const colors = [
          'green',
          'yellow',
          'grey',
        ];
  
  export default Vue.extend({
    data () {
      return {
        slides,
        colors,
      }
    },
  })
</script>