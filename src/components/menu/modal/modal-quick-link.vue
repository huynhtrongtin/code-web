<template>
  <div class="modal-quick-link">
    <div class="modal-quick-link-header">
      <div class="modal-quick-link-header-title">
        <h4>Quick Links</h4>
      </div>
      <div class="modal-quick-link-header-new">
        <span>1 NEW</span>
      </div>
    </div>
    <div class="modal-quick-link-content">
      <div class="modal-quick-link-content-group">
        <div
          class="modal-quick-link-content-group-item
          modal-quick-link-content-group-item--blue">
          <a href="#">
            <i class="fas fa-images"></i>
            <span>Gallery</span>
          </a>
        </div>
        <div
          class="modal-quick-link-content-group-item
          modal-quick-link-content-group-item--green">
          <a href="#">
            <i class="fas fa-envelope"></i>
            <span>Inbox</span>
          </a>
        </div>
        <div
          class="modal-quick-link-content-group-item
          modal-quick-link-content-group-item--red">
          <a href="#">
            <i class="fas fa-comments"></i>
            <span>Chat</span>
          </a>
        </div>
      </div>
      <div class="modal-quick-link-content-group">
        <div
          class="modal-quick-link-content-group-item
          modal-quick-link-content-group-item--red">
          <a href="#">
            <i class="fas fa-table"></i>
            <span>Tables</span>
          </a>
        </div>
        <div
          class="modal-quick-link-content-group-item
          modal-quick-link-content-group-item--bright-blue">
          <a href="#">
            <i class="far fa-calendar"></i>
            <span>Calendar</span>
          </a>
        </div>
        <div
          class="modal-quick-link-content-group-item
          modal-quick-link-content-group-item--yellow">
          <a href="#">
            <i class="far fa-user"></i>
            <span>User Profile</span>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
  .modal-quick-link {
    width: 300px;
    .modal-quick-link-header {
      display: flex;
      justify-content: space-between;
      background-color: #5d92f4;
      padding: 0 20px;
      border-radius: 10px 10px 0 0;
      .modal-quick-link-header-title {
        h4 {
          font-size: 20px;
        }
      }
      .modal-quick-link-header-new {
        display: flex;
        align-items: center;
        span {
          padding: 10px;
          border-radius: 10px;
          background-color: #ffb70f;
          font-size: 12px;
          font-weight: 600;
          color: #fff;
        }
      }
    }
    .modal-quick-link-content {
      display: flex;
      background-color: #fafafa;
      border-radius: 0 0 10px 10px;
      .modal-quick-link-content-group {
        width: 50%;
        .modal-quick-link-content-group-item {
          padding: 15px 10px;
          margin: 10px;
          background-color: #fff;
          box-shadow: 0 1px 5px 0px #666;
          span {
            margin-left: 10px;
          }
          a {
            color: #333;
          }
          &:hover {
            background-color: #f8f8f9;
          }
          &.modal-quick-link-content-group-item--blue {
            i {
              color: #5d92f4 !important;
            }
          }
          &.modal-quick-link-content-group-item--red {
            i {
              color: red !important;
            }
          }
          &.modal-quick-link-content-group-item--green {
            i {
              color: green !important;
            }
          }
          &.modal-quick-link-content-group-item--bright-blue {
            i {
              color: #00FFFF !important;
            }
          }
          &.modal-quick-link-content-group-item--yellow {
            i {
              color: yellow !important;
            }
          }
        }
      }
    }
  }
</style>
