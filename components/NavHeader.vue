<template>
  <div>
    <div class="d-flex align-items-center">
      <div class="mr-auto p-2">
        <div class="font-table" v-html="title"></div>
      </div>
      <div class="p-2">
        <b-form-input>ádfsdf</b-form-input>
        <b-input-group class="box-sh">
          <template #append>
            <b-input-group-text
              class="form-input-append" :class="status == true ? 'mouse-enter' : ''" @mouseenter="OnMouseEnter" @mouseleave="onMouseLeave"><b-icon icon="search" color="white" font-scale="0.9"></b-icon></b-input-group-text
            >
          </template>
          <b-form-input class="form-input placeholder-opacity" :class="status == true ? 'mouse-enter' : ''" @mouseenter="OnMouseEnter" @mouseleave="onMouseLeave" placeholder="Search">
            <!-- <div class="d-flex justify-content-end">
            <b-icon icon="search" color="white"></b-icon>
          </div> -->
          </b-form-input>
        </b-input-group>
      </div>
      <div class="p-2">
        <div class="name-user">
          <b-dropdown
            size="sm"
            variant="link"
            toggle-class="text-decoration-none"
            no-caret
          >
            <template #button-content>
              <b-avatar
                variant="info"
                src="https://placekitten.com/300/300"
              ></b-avatar>
              <span class="name">John Snow</span>
            </template>
            <div><span class="welcome">Welcome!</span></div>
            <b-dropdown-item href="#"
              ><span class="name-size d-flex align-items-center"
                ><b-icon icon="person-fill" font-scale="0.8"></b-icon>&ensp; My
                profile</span
              ></b-dropdown-item
            >
            <b-dropdown-item href="#">
              <span class="name-size d-flex align-items-center"
                ><b-icon icon="gear-fill" font-scale="0.8"></b-icon>&ensp;
                Settings</span
              ></b-dropdown-item
            >
            <b-dropdown-item href="#"
              ><span class="name-size d-flex align-items-center"
                ><b-icon icon="calendar-check-fill" font-scale="0.8"></b-icon
                >&ensp; Activity</span
              ></b-dropdown-item
            >
            <b-dropdown-item href="#"
              ><span class="name-size d-flex align-items-center"
                ><b-icon icon="alarm" font-scale="0.8"></b-icon>&ensp;
                Support</span
              >
            </b-dropdown-item>
            <hr />
            <b-dropdown-item href="#">
              <span class="name-size d-flex align-items-center"
                ><b-icon icon="box-arrow-left" font-scale="0.8"></b-icon
                >&ensp;Logout</span
              >
            </b-dropdown-item>
          </b-dropdown>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    let currentRoute = this.$route.path;
    let title = "TABLES";
    let status = false;
    return {
      currentRoute,
      title,
      status
    };
  },
  mounted() {
    if (this.$route.path == "/icons") {
      this.title = "ICONS";
    } else if (this.$route.path == "/") {
      this.title = "DASHBOARD";
    }
  },
  methods: {
    OnMouseEnter(){
      this.status = true;
    },
    onMouseLeave(){
      this.status = false;
    }
  },
  watch: {
    $route() {
      this.currentRoute = this.$route.path;
      if (this.currentRoute == "/icons") {
        this.title = "ICONS";
      } else if (this.currentRoute == "/") {
        this.title = "DASHBOARD";
      }
      console.log(this.$route.path);
    },
  },
};
</script>

<style scoped src="../assets/components/NavHeader/main.css"></style>
