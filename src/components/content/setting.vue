<template>
  <div class="setting">
    <div class="setting-icon" :style="{background: idColor}" @click="handleChangeSetting">
      <a href="#">
        <i class="fas fa-cog"></i>
      </a>
      <div class="modal-setting-parent">
      </div>
    </div>
  </div>
</template>
<script>

export default {
  props: [
    'idColor',
  ],
  data() {
    return {
      showModalSetting: false,
      hiddenScrollBar: false,
    };
  },
  methods: {
    handleChangeSetting() {
      this.hiddenScrollBar = !this.hiddenScrollBar;
      this.showModalSetting = !this.showModalSetting;
      this.$emit('changeSetting', this.showModalSetting);
      this.$emit('hiddenScrollBar', this.hiddenScrollBar);
    },
  },
};
</script>
<style lang="scss" scoped>
  .setting {
    right: 0;
    position: absolute;
    text-align: right;
    transform: translatey(200px);
    z-index: 1;
    .setting-icon {
      background-color: #5d92f4;
      padding: 10px;
      a {
        color: #fff;
        @-webkit-keyframes xoayvong{
          from{
              -webkit-transform:rotate(0deg);
              -moz-transform:rotate(0deg);
              -o-transform:rotate(0deg);
          }
          to{
              -webkit-transform:rotate(360deg);
              -moz-transform:rotate(360deg);
              -o-transform:rotate(360deg);
          }
        }
        @keyframes xoayvong {
          from{
              -webkit-transform:rotate(0deg);
              -moz-transform:rotate(0deg);
              -o-transform:rotate(0deg);
          }
          to{
              -webkit-transform:rotate(360deg);
              -moz-transform:rotate(360deg);
              -o-transform:rotate(360deg);
          }
        }
        i {
            animation: xoayvong 2s linear 0s infinite;
            -webkit-animation: xoayvong 2s linear 0s infinite;
            -moz-animation: xoayvong 2s linear 0s infinite;
            -o-animation: xoayvong 2s linear 0s infinite;
            font-size: 30px;
        }
      }
    }
  }
</style>
