<template>
  <div>
    <Slide/>
    <CardBox/>
    <Custom/>
  </div>
</template>
<script>
import Slide from '../components/Slide.vue'
import CardBox from '../components/FlexBox.vue'
import Custom from './Custom.vue';
export default {
  components: {
    Slide,
    CardBox,
    Custom
  }
}
</script>


<style lang="css" src="../css/common.css">
  
</style>