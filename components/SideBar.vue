<template>
  <div class="fixed-left">
    <div>
      <center>
        <img
          class="img-logo"
          src="https://demos.creative-tim.com/bootstrap-vue-argon-dashboard/img/brand/green.png"
        />
      </center>
    </div>
    <ItemSidebar content="Hello" icon="fa-check-circle"/>
  </div>
</template>

<script>
import ItemSidebar from './ItemSidebar.vue';
export default {
    components: {
        ItemSidebar
    }
}
</script>

<style scopped>
.fixed-left {
  display: block;
  position: fixed;
  top: 0;
  bottom: 0;
  width: 200px;
  background-color: white;
}
.img-logo {
  width: 120px;
  height: auto;
  margin-top: 20px;
}
</style>
