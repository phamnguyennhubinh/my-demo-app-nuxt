<template>
  <div class="d-flex">
    <div class="p-2">Hi</div>
    <div class="p-2"><i :class="iconClass"></i></div>
    <div class="p-6">{{ content }}</div>
  </div>
</template>

<script>
export default {
  props: {
    content: {
      type: String,
      required: true,
    },
    icon: {
      type: String,
      required: true,
    },
  },
  computed: {
    iconClass() {
      return ["fas", this.icon]; // assuming you're using Font Awesome's solid style
    },
  },
};
</script>

<style scopped>
.center-ver {
    text-align: center;
    vertical-align: middle;
}
</style>
