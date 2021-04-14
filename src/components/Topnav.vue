<template>
  <div class="topnav">
    <div class="logo">
      <img src="../assets/img/logopic.png" alt="">
    </div>
    <ul class="menu">
      <li>菜单1</li>
      <li>菜单2</li>
    </ul>
  </div>
</template>

<style lang="scss" scoped>
.topnav{
  background:#ffffff;
  display:flex;
  padding:16px;
  border-bottom:1px solid #DCDFE6;
  > .logo{
    max-width:32px;
    margin-right:auto;
    > img{
      max-width:32px;
      max-height:32px;
    }
  }
  > .menu{
    display: flex;
    white-space: nowrap;
    flex-wrap: nowrap;
    color:#8CC4FD;
    > li{
      margin:0 1em;
      line-height:32px;
    }
  }
}
</style>