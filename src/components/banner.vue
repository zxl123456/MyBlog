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
              <h4>Job Title</h4>
              <p>Web Designer and Developer</p>
            </div>
            <div class="banner-grids-left-info">
              <h4>Name</h4>
              <p>Xiaoli Zhu</p>
            </div>
            <div class="banner-grids-left-info">
              <h4>ADDRESS</h4>
              <p>ShenZhen</p>
            </div>
            <div class="banner-grids-left-info">
              <h4>EMAIL ADDRESS</h4>
              <p>845486385@qq.com</p>
            </div>
          </div>
          <div class="banner-grids-right">
            <div class="banner-right-img">
              <img src="../assets/1.jpg" alt="">
            </div>
            <div class="banner-right-info">
              <h2>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent scelerisque tellus dignissim dolor dignissim, sit amet convallis nisi dignissim.</h2>
              <p>Donec dolor felis, consectetur eget massa non, mattis euismod est. Nam augue neque, hendrerit nec scelerisque non, ultrices at ligula. Praesent posuere, turpis eget lobortis elementum, ex ante ultricies ligula, sit amet varius lacus dui in magna. Aliquam erat volutpat. Nulla condimentum, enim vitae congue ultrices, nibh erat efficitur sem, vel iaculis lectus eros in turpis. Aliquam venenatis cursus suscipit.</p>
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
