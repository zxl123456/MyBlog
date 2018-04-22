<template>
  <div class="projects" id="Projects">
    <div class="container">
      <div class="experience-tit">
        <h3>My Projects</h3>
      </div>
    </div>
    <div class="gw">
      <ul id="myTab" class="nav-tabs">
        <li :class="{on:curIndex==index?true:false}" @click="changeNav(index,item.type)" v-for="(item,index) in projectType"><a href="javascript:void(0);">{{ item.name }}</a></li>
      </ul>
      <div class="tab-content">
        <div class="tab-content-img">
          <div v-for="(item,index) in imgs" v-if="item.type==curType || curType=='all'">
            <a :href="item.url"><img :src="item.src"/></a>
            <div class="tab-content-ani">
              <p class="tab-content-bg"></p>
              <div class="tab-content-info">
                <p class="tab-content-info-tit">项目名</p>
                <p class="tab-content-info-content">项目简介项目简介项目简介项目简介项目简介项目简介项目简介项目简介项目简介项目简介项目简介项目简介项目简介项目简介项目简介项目简介项目简介项目简介项目简介项目简介项目简介</p>
                <p class="tab-content-time">项目完成时间</p>
              </div>
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
      return{
        projectType:[
          {name:"All",type:"all"},
          {name:"Apps",type:"app"},
          {name:"PC",type:"PC"},
          {name:"小程序",type:"小程序"}
        ],
        curIndex:0,
        curType:'all',
        imgs:[
          {src:require("../assets/p2.jpg"),url:'',type:'app'},
          {src:require("../assets/p3.jpg"),url:'',type:'app'},
          {src:require("../assets/p4.jpg"),url:'',type:'PC'},
          {src:require("../assets/p5.jpg"),url:'',type:'PC'},
          {src:require("../assets/p6.jpg"),url:'',type:'小程序'},
          {src:require("../assets/p3.jpg"),url:'',type:'app'},
          {src:require("../assets/p4.jpg"),url:'',type:'PC'},
          {src:require("../assets/p6.jpg"),url:'',type:'小程序'},
        ]
      }
    },
    methods:{
      changeNav(index,type){
        this.curIndex=index
        this.curType=type

      }
    }
  }
</script>

<style scoped>
  .projects{
    padding: 4em 0;
    box-sizing: border-box;
    background: #fff;
  }

.experience-tit h3{
  font-size: 2em;
  margin: 10px 0 30px;
  font-family: 'Roboto Slab', serif;
  font-weight: 700;
  letter-spacing: 1px;
  text-transform: uppercase;
  color: #2f2f2f;
}

  .nav-tabs{
    margin: 50px 0 40px;
  }

  .nav-tabs li{
    display: inline-block;
    padding: 13px 20px;
    border: 2px solid #333333;
    cursor: pointer;
    margin: 0 20px;
    transition: all .5s;
    -moz-transition: all .5s;
    -webkit-transition: all .5s;
  }

  .nav-tabs li a{
    color: #333333;
    display: block;
    transition: all .5s;
    -moz-transition: all .5s;
    -webkit-transition: all .5s;
  }

  .nav-tabs li.on,.nav-tabs li:hover{
    background: #ff9800;
    border: solid 2px #ff9800;
   /* -webkit-animation-name:shake;*/
    -webkit-animation-duration:.5s;
   /* -moz--name:shake;*/
    -moz-animation-duration:.5s;
  }

  .nav-tabs li.on a,.nav-tabs li:hover a{
    color: #fff;
  }

  .tab-content-img{
    display: flex;
    display: -webkit-flex;
    flex-direction: row;
    justify-content: space-between;
    flex-wrap: wrap;
  }

  .tab-content-img>div{
    width: 23%;
    margin-top: 2em;
    position: relative;
  }
  .tab-content-img img{
    width: 100%;
  }



  .tab-content-ani{
    cursor: pointer;
    opacity: 0;
    transition: all .5s;

  }

  .tab-content-ani .tab-content-bg,.tab-content-ani .tab-content-info{
    position: absolute;
    width: 100%;
    height: 100%;
    background: black;
    opacity: .3;
    left: 0;
    top: 0;
  }

  .tab-content-ani .tab-content-info{
    opacity: 1;
    background: initial;
    color: white;
  }

  .tab-content-ani .tab-content-info p{
    line-height: 30px;
  }

  .tab-content-info-tit{
    font-size: 16px;
    margin-top: 18px;
  }

  .tab-content-ani .tab-content-info .tab-content-info-content{
    text-align: left;
    width: 90%;
    margin: 0 auto;
    text-indent: 2em;
    font-size: 14px;
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-line-clamp: 3;
    overflow: hidden;
    line-height: 26px;
  }

  .tab-content-time{
    font-size: 14px;
    text-align: right;
    margin-right: 5%;
  }

  @-webkit-keyframes shake {
    0%, 100% {-webkit-transform: translateX(0);}
    30%,  70%,90% {-webkit-transform: translateX(-10px);}
    50%, 80% {-webkit-transform: translateX(10px);}
  }
  @-moz-keyframes shake {
    0%, 100% {-moz-transform: translateX(0);}
    30%,  70% ,90%{-moz-transform: translateX(-10px);}
    50%, 80% {-moz-transform: translateX(10px);}
  }


  .tab-content-img>div:hover .tab-content-ani{
    opacity: 1;
  }
</style>
