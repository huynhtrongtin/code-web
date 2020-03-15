<template>
  <div class="general-menu">
    <div class="general-menu-title">
      <h5>General</h5>
    </div>
    <div class="menu-group-list" @click="changeArrowDashboard = !changeArrowDashboard">
      <div class="menu-group-list-item-l" @click="showDashboard = !showDashboard">
        <a href="#" class="menu-group-list-item-l-header">
          <div class="menu-group-list-item-l-arrow">
            <i class="fas fa-caret-right" v-if="!changeArrowDashboard"></i>
            <i class="fas fa-sort-down" v-if="changeArrowDashboard"></i>
          </div>
          <div class="menu-group-list-item-s-right">
            <div class="menu-group-list-item-l-content">
            <i class="fas fa-columns"></i>
            <span>Dashboard</span>
            </div>
            <div class="menu-group-list-item-content-new">
              <span>New</span>
            </div>
          </div>
        </a>
        </div>
        <div class="menu-group-list-item-s-all" v-if="showDashboard">
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>E-Commerce</span>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>CRM</span>
              <div class="menu-group-list-item-content-new">
                <span>New</span>
              </div>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Crypto</span>
              <div class="menu-group-list-item-content-new">
                <span>New</span>
              </div>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Web Analytics</span>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Magazine</span>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>News</span>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Agency</span>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>SAAS</span>
            </a>
          </div>
        </div>
      </div>
      <div class="menu-group-list" @click="showCrypto = !showCrypto">
      <div class="menu-group-list-item-l" @click="changeArrowshowCrypto = !changeArrowshowCrypto">
        <a href="#" class="menu-group-list-item-l-header">
          <div class="menu-group-list-item-l-arrow">
            <i class="fas fa-caret-right" v-if="!changeArrowshowCrypto"></i>
            <i class="fas fa-sort-down" v-if="changeArrowshowCrypto"></i>
          </div>
          <div class="menu-group-list-item-s-right">
            <div class="menu-group-list-item-l-content">
            <i class="fas fa-wallet"></i>
            <span>Crypto</span>
            </div>
            <div class="menu-group-list-item-content-new">
              <span>New</span>
            </div>
          </div>
        </a>
        </div>
        <div class="menu-group-list-item-s-all" v-if="showCrypto">
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Market Cap</span>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Wallet</span>
              <div class="menu-group-list-item-content-new">
                <span>New</span>
              </div>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Trade</span>
              <div class="menu-group-list-item-content-new">
                <span>New</span>
              </div>
            </a>
          </div>
        </div>
      </div>
      <div class="menu-group-list" @click="showCRM = !showCRM">
      <div class="menu-group-list-item-l" @click="changeArrowshowCRM = !changeArrowshowCRM">
        <a href="#" class="menu-group-list-item-l-header">
          <div class="menu-group-list-item-l-arrow">
            <i class="fas fa-caret-right" v-if="!changeArrowshowCRM"></i>
            <i class="fas fa-sort-down" v-if="changeArrowshowCRM"></i>
          </div>
          <div class="menu-group-list-item-s-right">
            <div class="menu-group-list-item-l-content">
            <i class="fas fa-user-friends"></i>
            <span>CRM</span>
            </div>
            <div class="menu-group-list-item-content-new">
              <span>New</span>
            </div>
          </div>
        </a>
        </div>
        <div class="menu-group-list-item-s-all" v-if="showCRM">
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Projects</span>
              <div class="menu-group-list-item-content-new">
                <span>New</span>
              </div>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Project Details</span>
              <div class="menu-group-list-item-content-new">
                <span>New</span>
              </div>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Clients</span>
              <div class="menu-group-list-item-content-new">
                <span>New</span>
              </div>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Reportsx</span>
              <div class="menu-group-list-item-content-new">
                <span>New</span>
              </div>
            </a>
          </div>
        </div>
      </div>
      <div class="menu-group-list" @click="showCourses = !showCourses">
      <div class="menu-group-list-item-l" @click="changeArrowCourses = !changeArrowCourses">
        <a href="#" class="menu-group-list-item-l-header">
          <div class="menu-group-list-item-l-arrow">
            <i class="fas fa-caret-right" v-if="!changeArrowCourses"></i>
            <i class="fas fa-sort-down" v-if="changeArrowCourses"></i>
          </div>
          <div class="menu-group-list-item-s-right">
            <div class="menu-group-list-item-l-content">
            <i class="fas fa-book"></i>
            <span>Courses</span>
            </div>
          </div>
        </a>
        </div>
        <div class="menu-group-list-item-s-all" v-if="showCourses">
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Courses</span>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Courses List</span>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Courses Detail</span>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Sign In</span>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Payment</span>
            </a>
          </div>
        </div>
      </div>
      <div class="menu-group-list" @click="showWidgets = !showWidgets">
      <div class="menu-group-list-item-l" @click="changeArrowWidgets = !changeArrowWidgets">
        <a href="#" class="menu-group-list-item-l-header">
          <div class="menu-group-list-item-l-arrow">
            <i class="fas fa-caret-right" v-if="!changeArrowWidgets"></i>
            <i class="fas fa-sort-down" v-if="changeArrowWidgets"></i>
          </div>
          <div class="menu-group-list-item-s-right">
            <div class="menu-group-list-item-l-content">
            <i class="fas fa-th-large"></i>
            <span>Widgets</span>
            </div>
          </div>
        </a>
        </div>
        <div class="menu-group-list-item-s-all" v-if="showWidgets">
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>User</span>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Charts</span>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Trade</span>
              <div class="menu-group-list-item-content-new">
                <span>New</span>
              </div>
            </a>
          </div>
        </div>
      </div>
      <div class="menu-group-list" @click="showECommerce = !showECommerce">
      <div class="menu-group-list-item-l" @click="changeArrowECommerce = !changeArrowECommerce">
        <a href="#" class="menu-group-list-item-l-header">
          <div class="menu-group-list-item-l-arrow">
            <i class="fas fa-caret-right" v-if="!changeArrowECommerce"></i>
            <i class="fas fa-sort-down" v-if="changeArrowECommerce"></i>
          </div>
          <div class="menu-group-list-item-s-right">
            <div class="menu-group-list-item-l-content">
            <i class="fas fa-shopping-cart"></i>
            <span>E-Commerce</span>
            </div>
            <div class="menu-group-list-item-content-new">
              <span>New</span>
            </div>
          </div>
        </a>
        </div>
        <div class="menu-group-list-item-s-all" v-if="showECommerce">
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Shop With Algolia</span>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Shop</span>
              <div class="menu-group-list-item-content-new">
                <span>New</span>
              </div>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Product Detail</span>
              <div class="menu-group-list-item-content-new">
                <span>New</span>
              </div>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Add Product</span>
              <div class="menu-group-list-item-content-new">
                <span>New</span>
              </div>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Edit Product</span>
              <div class="menu-group-list-item-content-new">
                <span>New</span>
              </div>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Edit Detail</span>
              <div class="menu-group-list-item-content-new">
                <span>New</span>
              </div>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Cart</span>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Checkout</span>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Cards</span>
            </a>
          </div>
        </div>
      </div>
      <div class="menu-group-list" @click="showPages = !showPages">
      <div class="menu-group-list-item-l" @click="changeArrowPages = !changeArrowPages">
        <a href="#" class="menu-group-list-item-l-header">
          <div class="menu-group-list-item-l-arrow">
            <i class="fas fa-caret-right" v-if="!changeArrowPages"></i>
            <i class="fas fa-sort-down" v-if="changeArrowPages"></i>
          </div>
          <div class="menu-group-list-item-s-right">
            <div class="menu-group-list-item-l-content">
            <i class="fas fa-file"></i>
            <span>Pages</span>
            </div>
          </div>
        </a>
        </div>
        <div class="menu-group-list-item-s-all" v-if="showPages">
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Blog</span>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Gallery</span>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Pricing 1</span>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Pricing 2</span>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Blank</span>
            </a>
          </div>
        </div>
      </div>
      <div class="menu-group-list" @click="showSession = !showSession">
      <div class="menu-group-list-item-l" @click="changeArrowSession = !changeArrowSession">
        <a href="#" class="menu-group-list-item-l-header">
          <div class="menu-group-list-item-l-arrow">
            <i class="fas fa-caret-right" v-if="!changeArrowSession"></i>
            <i class="fas fa-sort-down" v-if="changeArrowSession"></i>
          </div>
          <div class="menu-group-list-item-s-right">
            <div class="menu-group-list-item-l-content">
            <i class="fas fa-clock"></i>
            <span>Session</span>
            </div>
          </div>
        </a>
        </div>
        <div class="menu-group-list-item-s-all" v-if="showSession">
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Sign Up</span>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Login</span>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Lock Screen</span>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Forgot Password</span>
            </a>
          </div>
          <div class="menu-group-list-item-s">
            <a href="#">
              <span>Reset Password</span>
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
      changeArrowDashboard: false,
      changeArrowshowCrypto: false,
      changeArrowshowCRM: false,
      changeArrowCourses: false,
      changeArrowWidgets: false,
      changeArrowECommerce: false,
      changeArrowPages: false,
      changeArrowSession: false,
      showDashboard: false,
      showCrypto: false,
      showCRM: false,
      showCourses: false,
      showWidgets: false,
      showECommerce: false,
      showPages: false,
      showSession: false,
    };
  },
};
</script>
<style lang="scss" scoped>
  .menu-group-list {
    margin: 35px 0;
    .menu-group-list-item-l {
      a {
        text-decoration: none;
      }
      i {
        color: #fff;
      }
      .menu-group-list-item-l-content {
        display: flex;
        i {
          font-size: 22px;
          margin-right: 10px;
        }
        span {
          color: #fff;
        }
      }
      .menu-group-list-item-content-new {
        color: #fff;
        background-color: red;
        border-radius: 3px;
        font-weight: 300;
        font-size: 10px;
        display: flex;
        align-items: center;
        padding: 5px;
      }
      .menu-group-list-item-l-header {
        display: flex;
        justify-content: space-between;
        .menu-group-list-item-s-right {
          display: flex;
          justify-content: space-between;
          width: 13vw;
        }
      }
    }
    .menu-group-list-item-s {
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
      .menu-group-list-item-content-new {
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
