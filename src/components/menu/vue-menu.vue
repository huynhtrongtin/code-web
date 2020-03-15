<template>
  <div class="v-menu"
    v-if="showMenu"
    :style="{background: idColorSidebar}">
    <div class="v-menu-content">
      <logo-menu/>
      <account-menu/>
      <general-menu/>
    </div>
  </div>
</template>
<script>
import LogoMenu from '@/components/menu/logo-menu.vue';
import AccountMenu from '@/components/menu/account-menu.vue';
import GeneralMenu from '@/components/menu/menu-content/general-menu.vue';

export default {
  props: [
    'showMenu',
    'idColorSidebar',
  ],
  components: {
    LogoMenu,
    AccountMenu,
    GeneralMenu,
  },
};
</script>
<style lang="scss" scoped>
  .v-menu {
    width: 22%;
    background-color: #2e3344;
    box-shadow: inset -1px 0px 5px 0.1px #eee;
    padding: 15px;
    color: #fff;
    font-family: Montserrat,sans-serif!important;
    position: relative;
  }
</style>
