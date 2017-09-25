<template>
  <div id="pubFooter">
    <div class="contact">
      <div class="container clearfix">
        <div class="left">
          <h2>关于<span>我们</span></h2>
          <p>作为中外知名的学校，引进一流的教育管理模式、融合国内外先进的教研成果、秉承最适合儿童成长的教育理念，同时，吸纳了经过百年验证的蒙台梭利教育精髓，拥有国际一流的教育专家团队和具有国际资格认证的中外教师队伍。</p>
          <p>每个校园都是按照国际纯正蒙台梭利校园的特点和标准精心设计的，充满着温馨关爱的教育氛，打造了最适合孩子健康成长的校园环境。</p>
        </div>
        <div class="right">
          <h2 class="bottomBorder"><span>联系</span>我们</h2>
          <img src="../../static/imgs/footer-1.png" alt="">
          <p>
            <svg class="icon" aria-hidden="true">
              <use xlink:href="#icon-position"></use>
            </svg>
            XXX省XXX市XXX县XXX路XXX号</p>
          <p>
            <svg class="icon" aria-hidden="true">
              <use xlink:href="#icon-tel"></use>
            </svg>
            <span>400-0000-000      |      020-00000000</span>
          </p>
          <p>
            <svg class="icon" aria-hidden="true">
              <use xlink:href="#icon-youxiang"></use>
            </svg>
            CONTACT@FKADJKHSF.CO
          </p>
        </div>
      </div>
    </div>
    <footer>
      <p>©2017 网站模板—学校 版权所有</p>
      <p>手机版 | 本站使用凡科建站搭建 | 管理登录</p>
    </footer>
  </div>
</template>

<style lang="scss" scoped>
#pubFooter{
  .contact {
    width: 100%;
    background: url(../../static/imgs/footerBg.jpg) 0 0/cover no-repeat;
    min-height: 375px;
    float: left;
    margin-top: -10px;
    padding-top: 10px;
    color: #ccc;
    .container {
      width: 1200px;
      margin: 40px auto;
      h2 {
        color: #fff;
        line-height: 3;
        font-size: 24px;
        font-weight: normal
      }
      span {
        color: #FF6537;
      }
      p {
        line-height: 2;
        font-size: 15px;
        margin-bottom: 20px;
      }
      .left {
        float: left;
        width: 570px;
        margin-right: 180px;
      }
      .right {
        float: left;
        width: 450px;
      }
      .icon {
        position: relative;
        top: 9px;
        padding: 5px;
        vertical-align: center;
        margin-right: 15px;
        font-size: 16px;
        width: 25px;
        height: 25px;
        background-color: #333;
        border-radius: 8px;
      }
    }
  }
  footer {
    float: left;
    padding: 30px 0;
    background-color: #212033;
    text-align: center;
    width: 100%;
    color: #aaa;
    font-size: 14px;
    line-height: 1.5;
  }
}
</style>
