<template>
  <div class="background-modal-setting" v-if="showModalSetting" @click="backgroundClose">
  </div>
</template>
<script>
export default {
  props: [
    'showModalSetting',
  ],
  methods: {
    backgroundClose() {
      this.$emit('backgroundClose', !this.showModalSetting);
    },
  },
};
</script>
<style lang="scss" scoped>
  .background-modal-setting {
    position: absolute;
    width: 100%;
    height: 100%;
    opacity: 0.46;
    background-color: rgb(33, 33, 33);
  }
</style>
