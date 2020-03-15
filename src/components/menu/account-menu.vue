<template>
  <div class="ac-menu">
    <div class="ac-menu-logo">
      <img src="/bulldog.png" alt="account">
    </div>
    <div class="ac-menu-name">
      <span>Trọng Tín</span>
    </div>
    <div class="ac-menu-select" @click="showModalAc=!showModalAc">
      <a><i class="fas fa-ellipsis-v"></i></a>
    </div>
    <div class="modal-ac-menu-select" v-if="showModalAc">
      <modal-account/>
    </div>
  </div>
</template>
<script>
import ModalAccount from '@/components/menu/modal/modal-account.vue';

export default {
  components: {
    ModalAccount,
  },
  data() {
    return {
      showModalAc: false,
    };
  },
};
</script>
<style lang="scss" scoped>
  .ac-menu {
    display: flex;
    justify-content: space-between;
    margin-top: 20px;
    .ac-menu-logo {
      img {
        width: 3vw;
        border-radius: 50%;
      }
    }
    .ac-menu-name {
      color: #fff;
      font-family: Montserrat,sans-serif!important;
      display: flex;
      align-items: center;
    }
    .ac-menu-select {
      padding: 10px 19px;
      font-size: 20px;
      display: flex;
      align-items: center;
      i {
        color: #fff;
      }
      &:hover {
        background-color: #585c69;
        border-radius: 50%;
      }
    }
    .modal-ac-menu-select {
      width: 100%;
      position: absolute;
      background-color: #FFF;
      transform: translateY(45px);
      background-color: #5d92f4;
      border-radius: 5px;
    }
  }
</style>
