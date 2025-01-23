<template>
  <div class="flex-row-between px-50 my-20">
    <div class="logo-img">
      <router-link to="">
        <img src="/public/img/logo.svg" alt="">
      </router-link>
    </div>
    <ul class="flex-row-between ga-20">
      <router-link v-for="(item, index) in headerItem" :key="index" :to="item.route" @click.native="showAlert(item.name)">
        <li>{{item.name}}</li>
      </router-link>
    </ul>
  </div>
</template>
<script>
export default {
  setup() {
    const headerItem = [
      { name: 'HOME', route: '/' },
      { name: 'ABOUT', route: '/' },
      { name: 'CONTACT', route: '/' },
    ]
    const showAlert = (menuName) => {
      alert(`"${menuName}" 서비스 준비중 입니다.`);
    };
    return {
      headerItem,
      showAlert
    }
  }
}
</script>

<style scoped>
.logo-img {
  width: calc(50% / 4);
}
.flex-row-between li {
  color: #333;
}
</style>