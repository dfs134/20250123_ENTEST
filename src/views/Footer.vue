<template>
  <div class="footer pa-30">
    <img src="/public/img/logo.svg" alt="">
    <h5 class="pt-20">CopyRights 2024. 테스트 All Rights Reserved</h5>
  </div>
</template>

<script>
export default {
  
}
</script>

<style scoped>
  .footer {
    color: #fff;
  }
  .footer img {
    width: calc(50% / 4);
  }
@media(max-width: 1240px) {
  .footer img {
    width: calc(50% / 2);
  }
}
</style>