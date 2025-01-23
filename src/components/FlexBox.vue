<template>
  <div class="flex-row-center items-start q-gutter-lg pt-50">
    <q-card class="my-card" v-for="(item, index) in slideItem" :key="index" :class="`shadow-${7}`">
      <img :src="item.src">
      <q-card-section>
        <div class="text-h6">{{item.text1}}</div>
        <div class="text-subtitle2">{{ item.text2 }}</div>
      </q-card-section>

      <q-card-section class="q-pt-none">
        {{ item.text3 }}
      </q-card-section>
    </q-card>

  </div>
</template>

<script>
export default {
  setup () {
    const slideItem = [
      {src : '/img/img1.jpg', text1:'Lorem ipsum dolor sit amet', text2:'Lorem ipsum dolor sit amet consectetur adipisicing elit.', text3:'Lorem ipsum dolor sit amet'},
      {src : '/img/img2.jpg', text1:'Lorem ipsum dolor sit amet', text2:'Lorem ipsum dolor sit amet consectetur adipisicing elit.', text3:'Lorem ipsum dolor sit amet'},
      {src : '/img/img3.jpg', text1:'Lorem ipsum dolor sit amet', text2:'Lorem ipsum dolor sit amet consectetur adipisicing elit.', text3:'Lorem ipsum dolor sit amet'},
      {src : '/img/img4.jpg', text1:'Lorem ipsum dolor sit amet', text2:'Lorem ipsum dolor sit amet consectetur adipisicing elit.', text3:'Lorem ipsum dolor sit amet'},
      
    ]
    return {
      slideItem,
    }
  }
}
</script>

<style scoped>
  .my-card {
    width: 250px;
  }
  .flex-row-center.items-start {
    flex-flow: row wrap;
  }
  .text-h6 {
    font-weight: bold;
    font-size: 24px;
  }
  .text-subtitle2 {
    font-size: 12px;
    font-weight: 300;
    padding-top: 10px;
    color: #666;
  }
  .q-pt-none {
    padding-top: 50px;
    font-size: 12px;
    font-weight: 300;
    color: #bbb;
  }
</style>