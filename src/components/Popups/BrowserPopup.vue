<template>
  <div class="browser-popup">
    <img
      src="@/assets/images/close-popup.svg"
      alt=""
      class="close-btn"
      @click="closePopup"
    />
    <p class="title text-start">请检查 Metamask 支持</p>

    <p class="p14 text-start">您需要使用 Google Chrome 或 Brave 浏览器</p>
  </div>
</template>

<script>
export default {
  methods: {
    closePopup() {
      this.$emit('close');
    },
  },
};
</script>

<style lang="scss" scoped></style>
