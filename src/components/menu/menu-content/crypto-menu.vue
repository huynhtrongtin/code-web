<template>
  <div class="crypto-menu">
    <div class="crypto-menu-title">
      <h5>Crypto</h5>
    </div>
    <div class="crypto-menu-group-list" @click="showCrypto = !showCrypto">
      <div class="crypto-menu-group-list-item-l" @click="changeArrow = !changeArrow">
        <a href="#" class="crypto-menu-group-list-item-l-header">
          <div class="crypto-menu-group-list-item-l-arrow">
            <i class="fas fa-caret-right" v-if="!changeArrow"></i>
            <i class="fas fa-sort-down" v-if="changeArrow"></i>
          </div>
          <div class="crypto-menu-group-list-item-l-content">
           <i class="fas fa-columns"></i>
           <span>Dashboard</span>
          </div>
          <div class="crypto-menu-group-list-item-content-new">
            <span>New</span>
          </div>
        </a>
        </div>
        <div class="crypto-menu-group-list-item-s-all" v-if="showCrypto">
          <div class="crypto-menu-group-list-item-s">
            <a href="#">
              <span>Market Cap</span>
            </a>
          </div>
          <div class="crypto-menu-group-list-item-s">
            <a href="#">
              <span>Wallet</span>
              <div class="crypto-menu-group-list-item-content-new">
                <span>New</span>
              </div>
            </a>
          </div>
          <div class="crypto-menu-group-list-item-s">
            <a href="#">
              <span>Trade</span>
              <div class="crypto-menu-group-list-item-content-new">
                <span>New</span>
              </div>
            </a>
          </div>
        </div>
      </div>
    </div>
</template>
<script>
export default {
  data() {
    return {
      changeArrow: false,
      showcrypto: false,
    };
  },
};
</script>
<style lang="scss" scoped>
  .crypto-menu-group-list {
    .crypto-menu-group-list-item-l {
      a {
        text-decoration: none;
      }
      i {
        color: #fff;
      }
      .crypto-menu-group-list-item-l-content {
        display: flex;
        i {
          font-size: 22px;
          margin-right: 10px;
        }
        span {
          color: #fff;
        }
      }
      .crypto-menu-group-list-item-content-new {
        color: #fff;
        background-color: red;
        border-radius: 3px;
        font-weight: 300;
        font-size: 10px;
        display: flex;
        align-items: center;
        padding: 5px;
      }
      .crypto-menu-group-list-item-l-header {
        display: flex;
        justify-content: space-between;
      }
    }
    .crypto-menu-group-list-item-s {
      padding: 20px;
      width: 14vw;
      display: flex;
      margin: 0 0 0 auto;
      justify-content: end;
      a {
        color: #fff;
        text-decoration: none;
        display: flex;
        width: 100%;
        justify-content: space-between;
      }
      .crypto-menu-group-list-item-content-new {
        span {
          color: #fff;
          background-color: red;
          border-radius: 3px;
          font-weight: 300;
          font-size: 10px;
          padding: 5px;
        }
      }
    }
  }
</style>
