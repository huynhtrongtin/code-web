<template>
  <div class="home-page-product">
    <div class="home-page-product-group">
      <div class="home-page-product-group-items">
        <button class="home-page-product-group-items-cart">
          <i class="fas fa-shopping-cart"></i>
        </button>
        <div class="home-page-product-group-items-info">
          <div class="home-page-product-group-items-img">
            <img src="1.jpg" alt="">
          </div>
          <div class="home-page-product-group-items-content">
            <div class="home-page-product-group-items-content-kind">
              <span>Jeans</span>
            </div>
            <div class="home-page-product-group-items-content-name">
              <h5>Vintage Jean</h5>
            </div>
            <div class="home-page-product-group-items-content-price">u
              <div class="home-page-product-group-items-content-price-sale">
                <span>$ 18.75</span>
              </div>
              <div class="home-page-product-group-items-content-price-real">
                <span>$16.75</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <ul v-for="(product, index) in allProduct" :key="`product-${index}`">
      <li><span>{{ product.id }}</span></li>
    </ul>
  </div>
</template>
<script>
import allProduct from '@/components/content/allProduct.js';

export default {
  data() {
    return {
      allProduct,
    };
  },
};
</script>
<style lang="scss" scoped>
  .home-page-product {
    width: 90%;
    margin: 0 auto;
    .home-page-product-group {
      .home-page-product-group-items {
        width: 22%;
        background-color: #fff;
        .home-page-product-group-items-cart {
          width: 55px;
          margin-left: auto;
          transform: translate(175px, 35px);
          border: none;
          background: transparent;
          i {
            font-size: 20px;
            border-radius: 50%;
            color: #fff;
            box-shadow: 0 3px 5px -1px rgba(0,0,0,.2),
            0 6px 10px 0 rgba(0,0,0,.14),
            0 1px 18px 0 rgba(0,0,0,.12);
            padding: 10px;
            cursor: pointer;
            background-color: #72a0f6;
            &:hover {
              background-color: #84abf4;
            }
            &:active {
              background-color: #5879b4;
            }
          }
        }
        .home-page-product-group-items-img {
          margin-top: -15px;
          img {
            widows: 205px;
            height: 262px;
          }
        }
        .home-page-product-group-items-content {
          .home-page-product-group-items-content-kind {
            span {
              font-family: Montserrat,sans-serif!important;
            }
          }
          .home-page-product-group-items-content-name {
            h5 {
              font-size: 20px;
            }
          }
          .home-page-product-group-items-content-price {
            .home-page-product-group-items-content-price-sale {
            }
            .home-page-product-group-items-content-price-real {
            }
          }
        }
      }
    }
  }
</style>
