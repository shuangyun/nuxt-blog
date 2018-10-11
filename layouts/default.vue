<template>
  <div>
    <el-container>

      <el-aside width="250px" class="aside">
        <div class="profile">
          <div 
            :class="`photo`"
            @click="onPhotoClick">
          </div>
          <div class="name">金众威</div>
        </div>

        <el-menu
          background-color="#202020"
          text-color="#fff"
          :router="true" >
          <el-menu-item index="/">
            <i class="el-icon-menu"></i>
            <span slot="title">首页</span>
          </el-menu-item>
          <el-menu-item index="archive">
            <i class="el-icon-date"></i>
            <span slot="title">归档</span>
          </el-menu-item>
          <el-menu-item index="tag">
            <i class="el-icon-document"></i>
            <span slot="title">标签</span>
          </el-menu-item>
          <el-menu-item index="about">
            <i class="el-icon-star-on"></i>
            <span slot="title">关于</span>
          </el-menu-item>
          <el-menu-item index="link">
            <i class="el-icon-share"></i>
            <span slot="title">友链</span>
          </el-menu-item>
          <el-menu-item index="search">
            <i class="el-icon-search"></i>
            <span slot="title">搜索</span>
          </el-menu-item>
        </el-menu>
      </el-aside>

      <el-main>
        <nuxt/>
      </el-main>

    </el-container>
  </div>
</template>

<script>
export default {
  name: 'defaultLayout',

  methods: {
    onPhotoClick () {
      window.location.href = window.location.origin
    }
  }
};
</script>

<style lang="less">
html {
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*, *:before, *:after {
  box-sizing: border-box;
  margin: 0;
}

.aside {
  background-color: #202020;
  height: 100vh;

  .profile {
    margin: 40px 0 10px 0;

    .photo {
      width: 140px;
      height: 140px;
      border-radius: 50%;
      overflow: hidden;
      margin: 0 auto;
      background-color: red;
      background-size: 140px 140px;
      background-repeat: no-repeat;
      cursor: pointer;
      background-image: url(~assets/jinzw.png);
    }

    .name {
      padding: 10px 0;
      font-size: 18px;
      color: #999;
      text-align: center;
    }
  }

  .el-menu {
    border-right: 0;

    .el-menu-item {
      font-size: 16px;
    }

    .el-menu-item [class^="el-icon-"] {
      font-size: 20px;
      margin-right: 20px;
    }
  }
}
</style>

