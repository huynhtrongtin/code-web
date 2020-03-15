<template>
  <div class="modal-ac-menu">
    <div class="modal-ac-menu-header">
      <h4>Trọng Tín</h4>
      <span>info@example.com</span>
    </div>
    <div class="modal-ac-menu-content">
      <div class="modal-ac-menu-content-select">
        <a href="#" class="modal-ac-menu-content-item">
          <i class="fas fa-user"></i>
          <h3>User Profile</h3>
        </a>
      </div>
      <div class="modal-ac-menu-content-select">
        <a href="#" class="modal-ac-menu-content-item">
          <i class="fas fa-envelope"></i>
          <h3>Inbox</h3>
        </a>
        </div>
      <div class="modal-ac-menu-content-select">
        <a href="#" class="modal-ac-menu-content-item">
          <i class="fas fa-bell"></i>
          <h3>Users List</h3>
        </a>
      </div>
      <div class="modal-ac-menu-content-select">
        <a href="#" class="modal-ac-menu-content-item">
          <i class="fas fa-sign-out-alt"></i>
          <h3>Log Out</h3>
        </a>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
  .modal-ac-menu-header {
    width: 100%;
    padding: 10px;
    color: #fff;
    transition: 2s;
    h4 {
      margin: 10px 0;
    }
    p {
      font-size: 15px;
    }
  }
  .modal-ac-menu-content {
    width: 100%;
    background-color: #fafafa;
    margin: 10px auto 0 auto;
    padding-top: 0.1px;
    padding-bottom: 0.1px;
    .modal-ac-menu-content-select {
      width: 90%;
      margin: 10px auto;
      background: #fff;
      box-shadow: 0 0 1px black;
      .modal-ac-menu-content-item {
        display: flex;
        text-decoration: none;
        color: #464d69;
        i {
          display: flex;
          align-items: center;
          font-size: 18.3px;
          margin: 0 10px 0 15px;
        }
        h3 {
          font-weight: 300;
          font-family: Montserrat, sans-serif !important;
        }
        &:hover {
          background-color: #fafafa;
          color: #5d92f4;
        }
      }
    }
  }
</style>
