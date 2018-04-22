<template>
  <div>
    <div class="menu" :class="{mopacity:isHidden}">
      <ul class="menu-list gw " >
        <li><a href="javascript:void (0)" @click="goNext(0)">Home</a></li>
        <li><a href="javascript:void (0)" @click="goNext(1)">About</a></li>
        <li><a href="javascript:void (0)" @click="goNext(2)">Experience</a></li>
        <li><a href="javascript:void (0)" @click="goNext(3)">Projects</a></li>
        <li><a href="javascript:void (0)" @click="goNext(4)">Contact</a></li>
      </ul>
    </div>
    <div class="m_nav" @click="showMenu">
      <div class="m_nav_ham" :class="{m_nav_ham_1_open:!isHidden}" id="m_ham_1"></div>
      <div class="m_nav_ham" :class="{m_nav_ham_2_open:!isHidden}"></div>
      <div class="m_nav_ham" :class="{m_nav_ham_3_open:!isHidden}"></div>
    </div>
  </div>
</template>

<script>
    export default {
        data(){
          return {
            isHidden:true
          }
        },
      methods:{
        showMenu(){
          this.isHidden=!this.isHidden
        },
        goNext(index){
          let scrollHeight= document.documentElement.scrollTop || document.body.scrollTop;
          document.documentElement.scrollTo(0,index*650)
        }
      }
    }
</script>

<style scoped>
  .menu{
    width: 100%;
    background-color: #fff;
    height: 120px;
    display: inline-block;
    position: fixed;
    z-index: 998;
    top: 0;
    left: 0;
    opacity: 1;
    transition: all 0.5s;
  }

  .mopacity{
    opacity: 0;
    display: none;
  }
  .menu-list{
    list-style: none;
    padding: 0;

  }

  .menu-list li{
    display: inline-block;
    line-height: 70px;
    margin: 25px 70px 25px 0;
  }

  .menu-list li a{
    color: #333;
    font-weight: 600;
    font-size: 18px;
    transition: color .5s;
  }

  .menu-list li a:hover{
    color:#FF9800;
  }

  .m_nav {
    position: fixed;
    top: 30px;
    right: 8.8%;
    z-index: 3;
    cursor: pointer;
    padding: .5em;
    background: rgba(130, 130, 130, 0.46);
    z-index: 999;
  }

  .m_nav_ham {
    width: 35px;
    height: 5px;
    background: #fff;
    margin: 5px auto;
    transition: all .5s;
  }

  .m_nav_ham_1_open {
    -webkit-transform: rotate(45deg);
    -moz-transform: rotate(45deg);
    -ms-transform: rotate(45deg);
    transform: rotate(45deg);
    margin-top: 15px;
  }
  .m_nav_ham_2_open {
    -webkit-transform: rotate(-45deg);
    -moz-transform: rotate(-45deg);
    -ms-transform: rotate(-45deg);
    transform: rotate(-45deg);
    margin-top: -10px;
  }
  .m_nav_ham_3_open {
    opacity: 0;
  }

  .button_open {
    background: #fff;
    -webkit-transform: rotate(45deg);
  }
</style>
