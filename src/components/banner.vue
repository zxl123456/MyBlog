<template>
  <div class="banner" id="Home" :style="{height:fullHeight}">
    <div class=" gw">
      <div class="agile-logo">
        <h1 ><a href="index.html">Creative<span>Resume</span></a></h1>
      </div>
    </div>
    <div class="gw">
      <div class="banner-grids">
          <div class="banner-grids-left">
            <div class="banner-grids-left-info">
                <h4>职位</h4>
              <p>前 端 工 程 师</p>
            </div>
            <div class="banner-grids-left-info">
              <h4>姓名</h4>
              <p>朱 小 丽</p>
            </div>
            <div class="banner-grids-left-info">
              <h4>目前所在地</h4>
              <p>深 圳</p>
            </div>
            <div class="banner-grids-left-info">
              <h4>  邮箱</h4>
              <p>845486385@qq.com</p>
            </div>
          </div>
          <div class="banner-grids-right">
            <div class="banner-right-img">
              <img src="../assets/1.jpg" alt="">
            </div>
            <div class="banner-right-info">
              <h2>我叫朱小丽，今年22岁，来自湖南永州，毕业于湖南工学院13级软件工程专业</h2>
              <p>于2017年毕业，算上实习期的一年，至今已工作近两年了，移动端及pc端的项目都有做过，移动端主要以框架为基础进行开发，如jqUI，superUI等轻框架，
              pc端主要是后台用到框架较多，如easyUI、bootStrap等。最近流行的框架及前端技术方面，有做过智能点餐的小程序，类似饿了么、美团。由于所在的公司没有用到vue、react以及rn等这些当下较为流行的技术，
              于是自己自学写了这几个相关的项目，具体请看我的个人技能展示及我的项目展示。</p>
            </div>
            <div class="banner-right-button">
              <div class="banner-right-button-info m_nav_item">
                <a class="hvr-sweep-to-bottom" href="#contact">Contact Me</a>
              </div>
            </div>

          </div>
      </div>
    </div>
  </div>
</template>

<script>
    export default {
      data(){
        return {
          fullHeight: document.documentElement.clientHeight+"px"

        }
      },
       mounted(){
         const that = this
         window.onresize = () => {
         return (() => {
           window.fullHeight = document.documentElement.clientHeight
           that.fullHeight = window.fullHeight
         })()
       }
       }
    }
</script>

<style scoped>
  *{
    font-size: 100%;
    font-family: 'Roboto Condensed', sans-serif;
  }
  .banner {
    background: url(../assets/6.jpg) no-repeat 0px 0;
    background-size: cover;
    padding: 0 0  5em 0;
    position: relative;
    display: inline-block;
    width: 100%;
  }
  .agile-logo {
    width: 13%;
    height: 70px;
    margin-top: 30px;
  }

  .agile-logo h1 a {
    color: #FFFfff;
    font-size: 18px;
    letter-spacing: 12px;
    font-family: 'Roboto Slab', serif;
    text-decoration: none;
  }

  .agile-logo h1 a span {
    display: block;
    font-size: 30px !important;
    font-weight: 700;
    letter-spacing: 6px;
    margin-top: 5px;
  }


  .banner-grids{
    padding: 30px 10px;
    margin-top: 20px;
    background: rgba(255, 255, 255, 0.18);
    display: inline-block;
    width: 100%;
  }

  .banner-grids .banner-grids-left{
    width: 31%;
    padding: 0 2%;
    float: left;
  }

  .banner-grids .banner-grids-right{
    width: 61%;
    padding: 0 2%;
    float: right;
  }

  .banner-grids-left-info {
    padding: 1em 0;
    border-bottom: 1px dashed #fff;
    text-align: left;
    color: #fff;
  }

  .banner-grids-left-info h4{
    font-size: 22px;
    margin: 0;
    font-family: 'Roboto Slab', serif;
    color: #FFFFFF;
    text-transform: uppercase;
    font-weight: 700;
    letter-spacing: 2px;
  }

  .banner-grids-left-info p{
    font-size: 14px;
    margin: 1em 0 0 0;
    color: #cecece;
  }

  .banner-right-img {
    float: left;
    width: 30%;
  }

  .banner-right-img img {
    width: 100%;
    border: solid 8px #ffffff;
  }

  img {
    vertical-align: middle;
  }

  .banner-right-info {
    float: right;
    width: 65%;
    text-align: left;
  }
  .banner-right-info h2 {
    color: #FFFFFF;
    font-size: 1em;
    font-weight: 600;
    margin: 0;
    line-height: 1.5em;
  }

  .banner-right-info p {
    color: #cecece;
    font-size: .9em;
    margin: 1em 0 0 0;
    line-height: 1.8em;
  }



</style>
