<template>
  <div id="app">
    <vue-menu :showMenu="showMenu" :idColorSidebar="idColorSidebar"/>
    <home-page :showMenu="showMenu" @changeShowMenu="handleChangeMenu" :idColor="idColor"/>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <background-modal-setting
      :showModalSetting="showModalSetting"
      @backgroundClose="handleShowSetting"/>
    <setting
      :idColor="idColor"
      @changeSetting="handleShowSetting"
      @hiddenScrollBar="handleHiddenScrollBar"
    />
      <transition name="fade">
        <modal-setting
          @changeColor="hadleChangeColor"
          :showModalSetting="showModalSetting"
          @changeColorSidebar="handleChangeColorSidebar"
        />
      </transition>
  </div>
</template>

<script>
import HelloWorld from '@/components/HelloWorld.vue';
import VueMenu from '@/components/menu/vue-menu.vue';
import HomePage from '@/components/content/home-page.vue';
import Setting from '@/components/content/setting.vue';
import ModalSetting from '@/components/menu/modal/modal-setting.vue';
import BackgroundModalSetting from '@/components/menu/modal/background-modal-setting.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
    VueMenu,
    HomePage,
    Setting,
    ModalSetting,
    BackgroundModalSetting,
  },
  data() {
    return {
      showMenu: false,
      idColor: '',
      showModalSetting: false,
      idColorSidebar: '',
      hiddenScrollBar: false,
    };
  },
  methods: {
    handleChangeMenu(payload) {
      this.showMenu = payload;
    },
    hadleChangeColor(payload) {
      this.idColor = payload;
    },
    handleShowSetting(payload) {
      this.showModalSetting = payload;
    },
    handleChangeColorSidebar(payload) {
      this.idColorSidebar = payload;
    },
    handleHiddenScrollBar(payload) {
      this.hiddenScrollBar = payload;
    },
  },
};
</script>

<style lang="scss">
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    display: flex;
  }
  a {
    text-decoration: none;
  }
  .fade-enter-active, .fade-leave-active {
    transition: opacity 1s;
  }
  .fade-enter, .fade-leave-to {
    opacity: 0;
  }
  .scroll-area {
    position: relative;
    margin: auto;
    width: 600px;
    height: 400px;
}
</style>
