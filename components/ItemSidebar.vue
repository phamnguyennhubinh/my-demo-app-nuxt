<template>
  <div id="itemSidebar">
    <ul>
      <li>
        <nuxt-link to="/">
          <b-icon icon="display" color="blue"></b-icon>
          <span :class="currentRoute == '/' ? 'active' : ''">Dashboard</span>
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/icons">
          <b-icon icon="alarm" color="blue"></b-icon> 
          <span :class="currentRoute == '/icons' ? 'active' : ''">Icons</span>
        </nuxt-link>
        
      </li>
      <li><b-icon icon="geo-alt-fill" color="red"></b-icon> Maps</li>
      <li><b-icon icon="person-fill" color="yellow"></b-icon> User Profile</li>
      <li><b-icon icon="list-ul" color="red"></b-icon> Tables</li>
      <li><b-icon icon="check2-all" color="blue"></b-icon> Login</li>
      <li><b-icon icon="person-circle" color="pink"></b-icon> Register</li>
    </ul>
    <hr class="margin-two" />
    <div class="title-document">DOCUMENTATION</div>
    <ul>
      <li><b-icon icon="alarm"></b-icon> Getting started</li>
      <li><b-icon icon="palette"></b-icon> Foundation</li>
      <li><b-icon icon="sticky-fill"></b-icon> Components</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    let currentRoute = this.$route.path;
    return {
      currentRoute
    };
  },
  watch: {
    $route() {
      this.currentRoute = this.$route.path;
      console.log(this.$route.path);
    },
  }
};
</script>

<style scopped src="../assets/components/ItemSidebar/main.css"></style>
