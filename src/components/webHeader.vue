<template>
  <div id="header">
    <header class="clearfix">
      <div class="container">
        <p>
          欢迎来到睦子荟！
          <span class="contact">
            <svg class="icon" aria-hidden="true">
              <use xlink:href="#icon-1"></use>
            </svg>
            icontact@fkadjkhsf.co 
          </span>
          <span class="contact">
            <svg class="icon" aria-hidden="true">
              <use xlink:href="#icon-3-copy"></use>
            </svg>
            400-000-0000
          </span>
        </p>
      </div>
    </header>
    <nav class="clearfix">
      <div class="container">
        <img src="../../static/imgs/logo.png" alt="睦子荟" class="logo">
        <transition name="fade">
          <ul>
            <li>首页</li>
            <li>睦子荟（关于我们）</li>
            <li>特色课程</li>
            <li>最新活动</li>
            <li>联系我们</li>
          </ul>
        </transition>
      </div>
    </nav>
  </div>
</template>

<script>
</script>

<style lang="scss" scoped>
#header{
  min-width: 1200px;
  .container{
    width: 1200px;
    margin: 0 auto;
  }
  header{
    background-color: rgb(98, 88, 187);
    color: #eee;
    line-height: 40px;
    .contact{
      margin-left: 15px;
      float: right;
      .icon{
        margin-right: 5px;
      }
    }
  }
  nav{
    width: 100%;
    margin: 0 auto;
    background-color: #fff;
    box-shadow: 0 2px 10px #ddd;
    .logo{
      float: left;
      height: 110px;
      line-height: 110px;
      cursor: pointer;
    }
    ul{
      float: right;
      li{
        float: left;
        line-height: 110px;
        margin-left: 20px;
        padding: 0 10px;
        cursor: pointer;
        transition: color .1s linear;
        &:hover{
          color: #ff6637;
        }
      }
    }
  }
}
</style>


