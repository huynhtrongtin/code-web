<template>
  <div class="modal-setting" v-if="showModalSetting">
    <div class="modal-setting-group">
      <div
        class="modal-setting-group-header"
        :style="{background: choseColor}">
        <h4>Theme Options</h4>
      </div>
      <div class="modal-setting-group-select">
        <div
          class="modal-setting-group-select-item"
          :class="{active: isLeftActive}"
          @click="handleLeftActive"
        >
          <span>General</span>
        </div>
        <div
          class="modal-setting-group-select-item"
          :class="{active: isRightActive}"
          @click="handleRightActive"
        >
            <span>Advance</span>
        </div>
      </div>
      <div class="modal-setting-group-content">
        <div class="modal-setting-group-content-box">
          <div class="modal-setting-group-content-box-title">
            <span>Select Theme</span>
          </div>
          <div class="modal-setting-group-content-box-color">
            <div
              class="modal-setting-group-content-box-color-item
              modal-setting-group-content-box-color-item--blue"
              @click="handleClick('#5d92f4')"
            >
            <div class="modal-setting-group-content-box-color-item-chose">
                <i class="far fa-circle chose"
                  id="item-blue"
                  v-if="choseColor === '#5d92f4'"
                ></i>
              </div>
            </div>
            <div
              class="modal-setting-group-content-box-color-item
              modal-setting-group-content-box-color-item--orange"
              @click="handleClick('#ffb70f')"
            >
              <div class="modal-setting-group-content-box-color-item-chose">
                  <i
                    class="far fa-circle"
                    id="item-orange"
                    v-if="choseColor === '#ffb70f'"
                  ></i>
              </div>
            </div>
            <div
              class="modal-setting-group-content-box-color-item
              modal-setting-group-content-box-color-item--green"
              @click="handleClick('#00d014')"
            >
              <div class="modal-setting-group-content-box-color-item-chose">
                  <i
                    class="far fa-circle"
                    id="item-green"
                    v-if="choseColor === '#00d014'"
                  ></i>
              </div>
            </div>
            <div
              class="modal-setting-group-content-box-color-item
              modal-setting-group-content-box-color-item--red"
              @click="handleClick('#ff3739')"
            >
              <div class="modal-setting-group-content-box-color-item-chose">
                  <i
                  class="far fa-circle"
                  id="item-red"
                  v-if="choseColor === '#ff3739'"
                  ></i>
              </div>
            </div>
            <div
              class="modal-setting-group-content-box-color-item
              modal-setting-group-content-box-color-item--bright-blue"
              @click="handleClick('#00d0bd')"
            >
              <div class="modal-setting-group-content-box-color-item-chose">
                  <i
                    class="far fa-circle"
                    id="item-bright-blue"
                    v-if="choseColor === '#00d0bd'"
                  ></i>
              </div>
            </div>
            <div
              class="modal-setting-group-content-box-color-item
              modal-setting-group-content-box-color-item--aqua"
              @click="handleClick('#82b1ff')"
            >
              <div class="modal-setting-group-content-box-color-item-chose">
                  <i
                    class="far fa-circle"
                    id="item-aqua"
                    v-if="choseColor === '#82b1ff'"
                  ></i>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="modal-setting-group-content">
        <div class="modal-setting-group-content-box">
          <div class="modal-setting-group-content-box-title">
            <span>Sidebar Filters</span>
          </div>
          <div class="modal-setting-group-content-box-color">
            <div
              class="modal-setting-group-content-box-color-item
              modal-setting-group-content-box-color-item"
              style="background: linear-gradient(180deg,#5d92f4,#09203f);"
              @click="handleClickSidebar('linear-gradient(180deg,#5d92f4,#09203f)')"
            >
            <div class="modal-setting-group-content-box-color-item-chose">
                <i class="far fa-circle chose"
                  id="item-blue"
                  v-if="choseColorSidebar === 'linear-gradient(180deg,#5d92f4,#09203f)'"
                ></i>
              </div>
            </div>
            <div
              class="modal-setting-group-content-box-color-item
              modal-setting-group-content-box-color-item--orange"
              style="background: linear-gradient(180deg,#b91372,#33080d);"
              @click="handleClickSidebar('linear-gradient(180deg,#b91372,#33080d)')"
            >
              <div class="modal-setting-group-content-box-color-item-chose">
                  <i
                    class="far fa-circle"
                    id="item-orange"
                    v-if="choseColorSidebar === 'linear-gradient(180deg,#b91372,#33080d)'"
                  ></i>
              </div>
            </div>
            <div
              class="modal-setting-group-content-box-color-item
              modal-setting-group-content-box-color-item--green"
              style="background: linear-gradient(0deg,#b02e0c,#ffb70f);"
              @click="handleClickSidebar('linear-gradient(0deg,#b02e0c,#ffb70f)')"
            >
              <div class="modal-setting-group-content-box-color-item-chose">
                  <i
                    class="far fa-circle"
                    id="item-green"
                    v-if="choseColorSidebar === 'linear-gradient(0deg,#b02e0c,#ffb70f)'"
                  ></i>
              </div>
            </div>
            <div
              class="modal-setting-group-content-box-color-item
              modal-setting-group-content-box-color-item--red"
              style="background: linear-gradient(0deg,#f53844,#42378f);"
              @click="handleClickSidebar('linear-gradient(0deg,#f53844,#42378f)')"
            >
              <div class="modal-setting-group-content-box-color-item-chose">
                  <i
                  class="far fa-circle"
                  id="item-red"
                  v-if="choseColorSidebar === 'linear-gradient(0deg,#f53844,#42378f)'"
                  ></i>
              </div>
            </div>
            <div
              class="modal-setting-group-content-box-color-item
              modal-setting-group-content-box-color-item--bright-blue"
              style="background: #2e3344;"
              @click="handleClickSidebar('#2e3344')"
            >
              <div class="modal-setting-group-content-box-color-item-chose">
                  <i
                    class="far fa-circle"
                    id="item-bright-blue"
                    v-if="choseColorSidebar === '#2e3344'"
                  ></i>
              </div>
            </div>
            <div
              class="modal-setting-group-content-box-color-item
              modal-setting-group-content-box-color-item--aqua"
              style="background: linear-gradient(180deg,#00d0bd,#007adf);"
              @click="handleClickSidebar('linear-gradient(180deg,#00d0bd,#007adf)')"
            >
              <div class="modal-setting-group-content-box-color-item-chose">
                  <i
                    class="far fa-circle"
                    id="item-aqua"
                    v-if="choseColorSidebar === 'linear-gradient(180deg,#00d0bd,#007adf)'"
                  ></i>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      isLeftActive: true,
      isRightActive: false,
      isChoseColor: false,
      choseColor: '#5d92f4',
      choseColorSidebar: '#2e3344',
    };
  },
  methods: {
    handleLeftActive() {
      this.isLeftActive = !this.isLeftActive;
      this.isRightActive = false;
    },
    handleRightActive() {
      this.isRightActive = !this.isRightActive;
      this.isLeftActive = false;
    },
    handleClick(id) {
      this.choseColor = id;
      this.$emit('changeColor', id);
    },
    handleClickSidebar(idColor) {
      this.choseColorSidebar = idColor;
      this.$emit('changeColorSidebar', idColor);
    },
  },
  props: [
    'showModalSetting',
  ],
};
</script>
<style lang="scss" scoped>
  .modal-setting {
    width: 25vw;
    position: absolute;
    right: 0;
    .modal-setting-group {
      .modal-setting-group-header {
        text-align: left;
        padding: 5px;
        background-color: #5d92f4;
        h4 {
          color: #fff;
          font-weight: 300;
          font-size: 20px;
          margin-left: 10px;
        }
      }
      .modal-setting-group-select {
        display: flex;
        .modal-setting-group-select-item {
          width: 50%;
          font-size: 25px;
          padding: 15px 0;
          background-color: #fff;
          text-align: center;
          cursor: pointer;
          span {
            color: #333;
          }
          &:hover {
            background-color: #eee;
          }
          &:active {
            border: 1px solid;
            box-shadow: inset 0 0 20px rgba(255, 255, 255, .5), 0 0 20px rgba(255, 255, 255, .2);
            outline-color: rgba(255, 255, 255, 0);
            outline-offset: 15px;
            text-shadow: 1px 1px 2px #427388;
          }
          &.modal-setting-group-select-item.active {
            span {
              color: #6094f4;
            }
            border-bottom: 2px solid #5d92f4;
          }
        }
      }
      .modal-setting-group-content {
        background-color: #fff;
        padding: 10px;
        .modal-setting-group-content-box {
          box-shadow: 0 0 3px 1px #eee;
          .modal-setting-group-content-box-title {
            text-align: center;
            margin-bottom: 15px;
            span {
              font-size: 20px;
              font-weight: 600;
            }
          }
          .modal-setting-group-content-box-color {
            display: flex;
            justify-content: center;
            .modal-setting-group-content-box-color-item {
              border-radius: 50%;
              font-size: 30px;
              margin: 5px;
              cursor: pointer;
              i {
                color: #fff;
                font-size: 27px;
              }
              .modal-setting-group-content-box-color-item-chose {
                display: flex;
                justify-content: center;
                align-items: center;
                width: 40.5px;
                height: 40.5px;
              }
              &.modal-setting-group-content-box-color-item--blue {
                background-color: #5d92f4;
              }
              &.modal-setting-group-content-box-color-item--orange {
                background-color: #ffb70f;
              }
              &.modal-setting-group-content-box-color-item--green {
                background-color: #00d014;
              }
              &.modal-setting-group-content-box-color-item--red {
                background-color: #ff3739;
              }
              &.modal-setting-group-content-box-color-item--bright-blue {
                background-color: #00d0bd;
              }
              &.modal-setting-group-content-box-color-item--aqua {
                background-color: #82b1ff;
              }
            }
          }
        }
      }
    }
  }
</style>
