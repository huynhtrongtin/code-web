<template>
  <div class="home-page">
    <div class="background-home-page" v-if="modalGrid > 0" @click="showModalGrid(0)">
    </div>
    <div class="home-page-header">
      <div class="home-page-header-left">
        <div class="home-page-header-left-menu">
          <a href="#">
           <i class="fas fa-bars" @click="changeShowMenu()"></i>
          </a>
        </div>
        <div
          class="home-page-header-left-quick-link"
          :class="{active: isActive}"
          @click="handleShowModalQuickLink"
        >
          <a href="#">
            <i class="fas fa-ellipsis-h"></i>
          </a>
          <transition name="fade">
            <div class="modal-header-left-quick-link"
              v-if="showModalQuickLink">
              <modal-quick-link/>
            </div>
          </transition>
        </div>
        <div
          class="home-page-header-left-search"
          :class="{clickSearch: isClickSearch}"
        >
          <div class="home-page-header-left-search-icon">
            <i class="fas fa-search"></i>
          </div>
          <div class="home-page-header-left-search-input" @click="eventClickSearch">
            <input type="text" placeholder="SEARCH">
          </div>
        </div>
      </div>
      <div class="home-page-header-right">
        <div class="home-page-header-right-button">
          <input type="button" value="Pricing" :style="{background: idColor}">
        </div>
        <div class="home-page-header-right-icon" @click="go_full_screen()">
          <a href="#"><i class="fas fa-compress"></i></a>
        </div>
        <div class="home-page-header-right-icon">
          <a href="#"><i class="fas fa-comments"></i></a>
        </div>
        <div class="home-page-header-right-icon">
          <a href="#"><i class="fas fa-bell" id="bellmove"></i></a>
        </div>
        <div class="home-page-header-right-icon">
          <a href="#"><i class="fas fa-shopping-cart"></i></a>
          <div class="cart-number-notify">
            <span>4</span>
          </div>
        </div>
        <div class="home-page-header-right-icon">
          <a href="#">
            <img src="img-nation/en.png" alt="EN">
          </a>
        </div>
      </div>
    </div>
    <div class="home-page-search">
      <div class="home-page-search-title">
        <h4>SEARCH</h4>
      </div>
      <div class="home-page-search-group">
        <div class="home-page-search-input">
          <div class="form__group field">
            <input
              type="input"
              class="inputfield"
              name="search"
              id="search"
              placeholder="Search"
              required
            >
            <label for="search" class="labelfield">Search</label>
          </div>
        </div>
        <div class="home-page-search-button">
          <input type="button" value="SEARCH">
        </div>
      </div>
    </div>
    <div class="home-page-project-grid">
      <div class="home-page-project-grid-group">
        <div class="home-page-project-grid-title">
          <h4>Project Grid</h4>
        </div>
        <div class="home-page-project-grid-text-right">
          <i
            class="fas fa-th"
            :class="{clickColor: isLeftClickColor}"
            @click="handleClickSort(1)"
          ></i>
          <i
            class="fas fa-list"
            :class="{clickColor: isRightClickColor}"
            @click="handleClickSort(2)"
          ></i>
        </div>
      </div>
      <div class="home-page-project-grid-dropdown-select">
        <div class="home-page-project-grid-dropdown-select-item">
          <div class="form__group field">
            <input
              type="input"
              class="inputfield inputfield--type"
              name="type"
              id="type"
              placeholder="Type"
              required
              @click="showModalGrid(1)"
              v-model="idItemType"
            >
            <i class="fas fa-sort-down" id="arrow"></i>
            <label
              for="type"
              class="labelfield labelfield--type"
            >Type</label>
          </div>
          <transition name=fade>
            <div class="modal-type" v-if="modalGrid === 1">
              <div class="modal-type-content">
                <div class="modal-type-content-item" @click="choseItemType('Men')">
                  <span>Men</span>
                </div>
                <div class="modal-type-content-item" @click="choseItemType('Women')">
                  <span>Women</span>
                </div>
                <div class="modal-type-content-item" @click="choseItemType('Gadgets')">
                  <span>Gadgets</span>
                </div>
                <div class="modal-type-content-item" @click="choseItemType('Accessories')">
                  <span>Accessories</span>
                </div>
              </div>
            </div>
          </transition>
        </div>
        <div class="home-page-project-grid-dropdown-select-item">
          <div class="form__group field">
            <input
              type="input"
              class="inputfield inputfield--type"
              name="recent"
              id="recent"
              placeholder="recent"
              required
              @click="showModalGrid(2)"
              v-model="idItemRecent"
            >
            <i class="fas fa-sort-down" id="arrow"></i>
            <label
              for="recent"
              class="labelfield labelfield--type"
            >Recent</label>
          </div>
          <transition name=fade>
            <div class="modal-type" v-if="modalGrid === 2">
              <div class="modal-type-content">
                <div class="modal-type-content-item" @click="choseItemRecent('This Week')">
                  <span>This Week</span>
                </div>
                <div class="modal-type-content-item" @click="choseItemRecent('This Month')">
                  <span>This Month</span>
                </div>
                <div class="modal-type-content-item" @click="choseItemRecent('Past Month')">
                  <span>Past Month</span>
                </div>
              </div>
            </div>
          </transition>
        </div>
        <div class="home-page-project-grid-dropdown-select-item">
          <div class="form__group field">
            <input
              type="input"
              class="inputfield inputfield--type"
              name="no-of-items"
              id="no-of-items"
              placeholder="No of Items"
              required
              @click="showModalGrid(3)"
              v-model="idNoOfItems"
            >
            <i class="fas fa-sort-down" id="arrow"></i>
            <label
              for="no-of-items"
              class="labelfield labelfield--type"
            >No of Items</label>
          </div>
          <transition name=fade>
            <div class="modal-type" v-if="modalGrid === 3">
              <div class="modal-type-content">
                <div class="modal-type-content-item" @click="choseItemNOItem('10')">
                  <span>10</span>
                </div>
                <div class="modal-type-content-item" @click="choseItemNOItem('20')">
                  <span>20</span>
                </div>
                <div class="modal-type-content-item" @click="choseItemNOItem('30')">
                  <span>30</span>
                </div>
              </div>
            </div>
          </transition>
        </div>
      </div>
    </div>
    <home-page-product/>
  </div>
</template>
<script>
import ModalQuickLink from '@/components/menu/modal/modal-quick-link.vue';
import HomePageProduct from '@/components/content/home-page-product.vue';

export default {
  props: [
    'showMenu',
    'idColor',
  ],
  components: {
    ModalQuickLink,
    HomePageProduct,
  },
  methods: {
    changeShowMenu() {
      this.$emit('changeShowMenu', !this.showMenu);
    },
    handleShowModalQuickLink() {
      this.showModalQuickLink = !this.showModalQuickLink;
      this.isActive = !this.isActive;
      this.moveModal = !this.moveModal;
    },
    go_full_screen() {
      const elem = document.documentElement;
      if (elem.requestFullscreen) {
        elem.requestFullscreen();
      } else if (elem.msRequestFullscreen) {
        elem.msRequestFullscreen();
      } else if (elem.mozRequestFullScreen) {
        elem.mozRequestFullScreen();
      } else if (elem.webkitRequestFullscreen) {
        elem.webkitRequestFullscreen();
      }
    },
    eventClickSearch() {
      this.isClickSearch = !this.isClickSearch;
    },
    showModalGrid(id) {
      this.modalGrid = id;
    },
    choseItemType(type) {
      this.idItemType = type;
      this.modalGrid = 0;
    },
    choseItemRecent(recent) {
      this.idItemRecent = recent;
      this.modalGrid = 0;
    },
    choseItemNOItem(noOfItem) {
      this.idNoOfItems = noOfItem;
      this.modalGrid = 0;
    },
    handleClickSort(id) {
      if (id === 1) {
        this.isLeftClickColor = true;
        this.isRightClickColor = false;
      } else {
        this.isLeftClickColor = false;
        this.isRightClickColor = true;
      }
    },
  },
  data() {
    return {
      showModalQuickLink: false,
      isActive: false,
      isClickSearch: false,
      modalGrid: 0,
      idItemType: '',
      idItemRecent: '',
      idNoOfItems: '',
      isLeftClickColor: true,
      isRightClickColor: false,
    };
  },
};
</script>
<style lang="scss" scoped>
  .home-page {
    width: 100%;
    background-color: #f4f7fa;
    input {
      border: none;
      border-bottom: 1px solid #333;
    }
    .inputfield {
      font-family: inherit;
      width: 40vw;
      border: 0;
      border-bottom: 2px solid #9b9b9b;
      outline: 0;
      font-size: 1.3rem;
      color: #fff;
      padding: 7px 0;
      background: transparent;
      transition: border-color 0.2s;
      cursor: pointer;
      &::placeholder {
        color: transparent;
      }
      &:placeholder-shown ~ .labelfield {
        font-size: 1.3rem;
        cursor: text;
        top: 20px;
        transform: translateY(150px);
      }
      &.inputfield.inputfield--type {
        width: 15vw;
      }
    }
    .labelfield {
      position: absolute;
      top: 100;
      display: block;
      transition: 0.2s;
      font-size: 1rem;
      color: #9b9b9b;
      &.labelfield.labelfield--type {
        top: 5px;
        transform: translateY(425px);
        cursor: pointer;
      }
    }
    .inputfield:focus {
      ~ .labelfield {
        position: absolute;
        top: 100;
        display: block;
        transition: 0.2s;
        font-size: 1rem;
        color: #11998e;
        font-weight:700;
      }
      padding-bottom: 6px;
      font-weight: 700;
      border-width: 3px;
      border-image: linear-gradient(to right, #11998e, #38ef7d);
      border-image-slice: 1;
    }
    .inputfield{
      &:required,&:invalid { box-shadow:none;color:#333; }
    }
    .home-page-header {
      background-color: #f5f5f5;
      display: flex;
      justify-content: space-between;
      padding: 10px 0;
      box-shadow: 0 4px 15px 0 rgba(0,0,0,.09);;
      .home-page-header-left {
        display: flex;
        i {
          color: #333;
          font-size: 25px;
          margin: 10px 20px;
          padding: 5px;
        }
        .home-page-header-left-menu {
          &:hover {
            background-color: #e3e3e3;
            border-radius: 50%;
          }
          &:active {
            background-color: #666;
            margin-top: 5px;
          }
        }
        .home-page-header-left-quick-link {
          &:hover {
            background-color: #e3e3e3;
            border-radius: 50%;
          }
          &:active {
            background-color: #666;
          }
          &.home-page-header-left-quick-link.active {
            background-color: #e3e3e3;
            border-radius: 50%;
          }

          .modal-header-left-quick-link {
            position: absolute;
            transform: translate(15px, -15px);
          }
        }
        .home-page-header-left-search {
          display: flex;
          margin: auto 0;
          border: 1px solid #333;
          border-radius: 5px;
          input {
            height: 35px;
            border: none;
            background-color: #f5f5f5;
            &:focus {
              outline: none;
            }
          }
          &.home-page-header-left-search.clickSearch {
            border: 1px solid #5d92f4;
            padding-right: 10px;
            i {
              color: #5d92f4;
            }
          }
          .home-page-header-left-search-input {
            display: flex;
            align-items: center;
          }
        }
      }
      .home-page-header-right {
        display: flex;
        i {
          font-size: 30px;
          color: #727891;
        }
        .home-page-header-right-icon {
          margin: auto 0;
          padding: 10px;
          &:hover {
            background-color: #e3e3e3;
            border-radius: 50%;
          }
          #bellmove:hover {
            animation: shake 0.5s;
            animation-iteration-count: infinite;
          }
          @keyframes shake {
            0% { transform: translate(1px, 1px) rotate(0deg); }
            10% { transform: translate(-1px, -2px) rotate(-1deg); }
            20% { transform: translate(-3px, 0px) rotate(1deg); }
            30% { transform: translate(3px, 2px) rotate(0deg); }
            40% { transform: translate(1px, -1px) rotate(1deg); }
            50% { transform: translate(-1px, 2px) rotate(-1deg); }
            60% { transform: translate(-3px, 1px) rotate(0deg); }
            70% { transform: translate(3px, 1px) rotate(-1deg); }
            80% { transform: translate(-1px, -1px) rotate(1deg); }
            90% { transform: translate(1px, 2px) rotate(0deg); }
            100% { transform: translate(1px, -2px) rotate(-1deg); }
          }
        }
        .home-page-header-right-button {
          margin: auto 0;
          margin-right: 5px;
          input {
            background-color: #5d92f4;
            height: 46px;
            width: 94px;
            color: #fff;
            font-size: 20px;
            border-radius: 8px;
            border: none;
            outline: none;
            &:active {
              background-color: #7ba7fa;
            }
            &:hover {
              background-color: #7ba7fa;
            }
          }
        }
      }
    }
    .home-page-search {
      width: 90%;
      display: flex;
      justify-content: space-around;
      margin: 40px auto;
      background-color: #fff;
      padding: 20px;
      box-shadow: 0 0 5px 0px #999;
      .home-page-search-title {
        h4 {
          font-size: 25px;
        }
      }
      .home-page-search-group {
        display: flex;
        align-items: center;
        .home-page-search-input {
          margin-right: 20px;
        }
        .home-page-search-button {
          input {
            height: 46px;
            width: 94px;
            color: #fff;
            font-size: 20px;
            border: none;
            outline: none;
            cursor: pointer;
            background-color: #5d92f4;
            border-radius: 10px;
            &:hover {
              background-color: #80a7ef;
            }
            &:active {
              background-color: #436cb8;
            }
          }
        }
      }
    }
    .home-page-project-grid {
      width: 90%;
      padding: 20px;
      margin: 0 auto;
      .home-page-project-grid-group {
        display: flex;
        justify-content: space-between;
        .home-page-project-grid-title {
          h4 {
            font-size: 25px;
          }
        }
        .home-page-project-grid-text-right {
          margin: auto 0;
          i {
            font-size: 20px;
            margin-right: 10px;
            color: #999;
            cursor: pointer;
            &:active {
              color: #333;
            }
            &.clickColor {
              color: #333;
            }
          }
        }
      }
      .home-page-project-grid-dropdown-select {
        display: flex;
        .home-page-project-grid-dropdown-select-item {
          margin: 20px;
          .inputfield:focus + #arrow {
            color: #38ef7d;
            transform: rotate(180deg);
            transition: 2s;
          }
          i {
            position: absolute;
            transform: translate(-20px,-10px);
            font-size: 25px;
            color: #999;
          }
          .modal-type {
            .modal-type-content {
              width: 15vw;
              background-color: #fff;
              transform: translateY(-25px);
              box-shadow: 0 0 10px #999;
              position: absolute;
              .modal-type-content-item {
                padding: 20px;
                cursor: pointer;
                span {
                  font-size: 15px;
                  font-weight: 600;
                }
                &:hover {
                  background-color: #f8f8f9;
                }
                &:active {
                  background-color: #dddde1;
                }
              }
            }
          }
        }
      }
    }
    .background-home-page {
      width: 100%;
      height: 100%;
      position: absolute;
      background-color: transparent;
    }
  }
</style>
