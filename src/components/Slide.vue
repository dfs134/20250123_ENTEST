<template>
  <div class="">
    <q-carousel
      animated
      v-model="slide"
      navigation
      infinite
      :autoplay="autoplay"
      arrows
      transition-prev="slide-right"
      transition-next="slide-left"
      @mouseenter="autoplay = false"
      @mouseleave="autoplay = true"
    >
      <router-link to="#" v-for="(item, index) in slideItem" :name="item.name" :key="index">
        <q-carousel-slide class="column no-wrap flex-center" :img-src="item.src" >
          <div class="width-fill">
            <div class="text-width">
              <h3 class="q-pl-md q-mt-md" v-bind:class="item.bgColor">
              {{item.text1}}
              </h3>
              <h5 class="q-pl-md pt-30" v-bind:class="item.bgColor">
                {{item.text2}}
              </h5>
            </div>
          </div>
        </q-carousel-slide>
      </router-link>
    </q-carousel>
  </div>
</template>

<script>
import { ref } from 'vue'
export default {
  setup () {
    const slideItem = [
      {src : '/img/img1.jpg', bgColor:'text-white', name: 1, text1:'Lorem ipsum dolor sit amet', text2:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Nostrum aperiam corporis eligendi placeat sed nihil '},
      {src : '/img/img2.jpg', bgColor:'text-black', name: 2, text1:'Lorem ipsum dolor sit amet', text2:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Nostrum aperiam corporis eligendi placeat sed nihil '},
      {src : '/img/img3.jpg', bgColor:'text-white', name: 3, text1:'Lorem ipsum dolor sit amet', text2:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Nostrum aperiam corporis eligendi placeat sed nihil '},
      {src : '/img/img4.jpg', bgColor:'text-black', name: 4, text1:'Lorem ipsum dolor sit amet', text2:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Nostrum aperiam corporis eligendi placeat sed nihil '}
    ]
    return {
      slide: ref(1),
      autoplay: ref(true),
      slideItem,
    }
  },
}
</script>

<style scoped>
  .column {
    color: #333;
  }
  .text-width {
    /* width: calc(100% / 5); */
    margin-left: 150px;
  }
  .text-width h3, .text-width h5 {
    width: 350px;
  }
</style>