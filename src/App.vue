<template>
    <div>
      <div class="QRcode">
        <p>微信扫描二维码，手机打开预览效果最佳噢</p>
        <img src="../src/assets/QRcode.png" alt="手机打开的二维码">
      </div>
        <router-view></router-view>
    </div>
</template>

<style lang="scss">
    @import "~@/assets/style/helper.scss";
    @import "~@/assets/style/reset.scss";
    body{
        line-height: 1.5;
        font-size: 16px;
        font-family: $font-hei;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        background: #FCF5F7;
      // 让电脑端不那么太难看
      max-width: 640px;
      margin: 0 auto;
    }
    .QRcode{
      display: none;
    }
    @media (min-width: 768px) {
      .QRcode{
        display: block;
        position: fixed;
        width: 120px;
        height: 120px;
        right: 100px;
        top: 50px;
        > img{
          width: 100%;
        }
        > p{
          color: green;
          font-weight: bolder;
        }
      }
    }
</style>
