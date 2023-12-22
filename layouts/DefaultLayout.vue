<template>
  <div class="posi-relate">
    <SideBar />
    <Header />
    <div class="margin-left">
      <div class="container index-top-content padding-container">
        <Nuxt />
      </div>
    </div>
  </div>
</template>

<script>
import SideBar from "../components/SideBar.vue";
import Header from "../components/Header.vue";

export default {
  components: {
    SideBar,
    Header,
  },
  setup() {},
};
</script>

<style scoped>
.index-top-content {
  z-index: 3;
}
.margin-left {
  position: absolute;
  margin-left: 200px;
  top: 100px;
}
.posi-relate {
  position: relative;
}
.padding-container {
  padding-left: 40px;
  padding-right: 40px;
}
</style>
