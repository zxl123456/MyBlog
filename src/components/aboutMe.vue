<template>
  <div id="About" class="about-me clearfix">
    <div class="gw">
      <div class="about-me-left">
        <h3>About Me</h3>
        <h4>Mauris molestie ultrices molestie. Sed rhoncus interdum ipsum, id fermentum sem pellentesque ut.</h4>
        <p>Praesent egestas egestas felis, sit amet posuere massa malesuada eget. Phasellus sem urna, euismod sit amet orci laoreet, laoreet molestie purus. Nulla leo purus, blandit nec efficitur tempor, interdum vel enim. <span>Proin mauris mi, lobortis quis quam at, tristique dictum arcu. In lobortis, massa in porta posuere, orci orci tincidunt risus, vitae ultrices enim eros vel lacus.</span>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent tincidunt tellus at est fermentum ultricies. Cras cursus semper libero. Vivamus non elit a diam elementum vulputate ac quis nisi. Suspendisse tellus massa, tempus in tristique a, eleifend non est. Duis consequat facilisis laoreet. </p>
      </div>
      <div class="about-me-right">
        <h3 style="margin-bottom: 0;">Skills</h3>
        <div class="skills-bar" style="height: 400px;" id="myChart">

        </div>
      </div>
    </div>

  </div>
</template>

<script>
  export default {
    data(){
      return{
        skillData:[
          { name: 'html/css', value: 90 },
          { name: 'html5/css3', value: 85 },
          { name: 'javascript', value: 70 },
          { name: 'jquery', value: 85 },
          { name: 'vue', value: 70 },
          { name: '小程序', value: 80 },
          { name: 'react', value: 80 },
          { name: 'easyUI', value: 80 },
          { name: 'jqUI', value: 70 },
          { name: 'webpack', value: 50 },
          { name: 'SVN',  value: 70 },
          { name: 'bootStrap',  value: 70 }
          ],
        skillSymboData:[
          { name: 'html/css', value: 90, "symbolSize": 30  },
          { name: 'html5/css3', value: 85, "symbolSize": 25 },
          { name: 'javascript', "symbolSize": 20, value: 70, },
          { name: 'jquery', "symbolSize": 25, value: 85},
          { name: 'vue', "symbolSize": 20, value: 70 },
          { name: '小程序', "symbolSize": 25, value: 80 },
          { name: 'react', "symbolSize": 25, value: 80 },
          { name: 'easyUI', "symbolSize": 25,  value: 80 },
          { name: 'jqUI', "symbolSize": 25, value: 70 },
          { name: 'webpack', "symbolSize": 10, value: 50},
          { name: 'SVN', "symbolSize": 20, value: 70},
          { name: 'bootStrap', "symbolSize": 20, value: 70}
          ]
      }
    },
    computed:{
    },
    mounted(){
      this.drawMySkill()
    },
    methods:{
      roundDatas(num) {
        let datas = [];
        for (let i = 0; i < num; i++) {
          datas.push({
            name: 'circle' + i
          });
        }
        return datas;
      },
      drawMySkill(){
        let myChart = this.$echarts.init(document.getElementById('myChart'));
        myChart.setOption({
          title: {
            text: '个人技能',
            top: "center",
            left: "center",
            textStyle: {
              fontSize: 18,
              color: '#9474B4',
              fontWeight: 'bolder'
            }
          },
          animationDurationUpdate: 1500,
          animationEasingUpdate: 'quinticInOut',
          roam: false, //鼠标缩放及平移
          focusNodeAdjacency: true, //是否在鼠标移到节点上的时候突出显示节点以及节点的边和邻接节点
          dataRange: {
            min: 0,
            max: 60,
            y: '100%',
            calculable: true,
            show: false,
            color: ['#59446B', '#D69BFF']
          },
          series: [{
            name: '',
            type: 'pie',
            startAngle: 0,
            hoverAnimation: false,
            radius: ['60%', '60%'],
            center: ['50%', '50%'],
            data: this.skillData,
            itemStyle: {
              normal: {
                color: '#000',
                borderWidth: 5,
                borderColor: 'rgba(0,0,0,0)',
                label: {
                  show: true,
                  formatter: '{b}\n熟练程度：{c}%',
                },
                labelLine: {
                  show: true,
                  length: 40,
                  lineStyle: {
                    color: '#7C9ECD'
                  }
                }
              }
            }
          }, {
            type: 'graph',
            tooltip: {},
            ribbonType: true,
            layout: 'circular',
            hoverAnimation: false,
            width: '60%',
            height: '60%',
            circular: {
              rotateLabel: true
            },
            symbolSize: 1,
            data: this.roundDatas(300),
            itemStyle: {
              normal: {
                label: {
                  show: false
                },
                color: '#58446C',
              },
              emphasis: {
                label: {
                  show: false,
                }
              }
            },
          }, {
            type: 'graph',
            tooltip: {},
            ribbonType: true,
            layout: 'circular',
            width: '60%',
            height: '60%',

            circular: {
              rotateLabel: true
            },
            symbolSize: 30,
            label: {
              normal: {
                position: 'center',
                formatter: '{b}\n熟练程度：{d}%',
                normal: {
                  textStyle: {
                    fontFamily: '宋体'
                  }
                }
              }
            },
            edgeSymbol: ['circle'],
            edgeSymbolSize: [8, 10],
            edgeLabel: {
              normal: {
                textStyle: {
                  fontSize: 13,
                  fontWeight: 'bold',
                  fontFamily: '宋体'
                }
              }
            },
        itemStyle: {
              normal: {
                label: {
                  rotate: true,
                  show: false,
                  textStyle: {
                    color: '#9474B4',
                  }
                },
                borderColor: '#7C9ECD',
                borderWidth: 3,

              },
              emphasis: {
                label: {
                  show: false,
                }
              }
            },

            data: this.skillSymboData
          }]
        });
      },
    }
  }
</script>

<style scoped>
  *{
    text-align: left;
  }
  .about-me{
    padding: 60px 0;
    box-sizing: border-box;
    background: #fff;
  }
  .about-me-left{
    width: 49%;
    float: left;
  }
  .about-me-right{
    width: 49%;
    float: right;
  }
  .about-me-left h3,.about-me-right h3{
    color: #2f2f2f;
    font-size: 2em;
    margin: 0 0 1em 0;
    font-family: 'Roboto Slab', serif;
    font-weight: 700;
    letter-spacing: 1px;
    text-transform: uppercase;
  }

  .about-me-left h4 {
    color: #2f2f2f;
    font-size: 1em;
    font-weight: 600;
    margin: 0;
    line-height: 1.5em;
  }

  .about-me-left p {
    color: #999999;
    font-size: .9em;
    margin: 1em 0 0 0;
    line-height: 1.8em;
  }
  .skills-bar-content{
    position: relative;
    margin-bottom: 20px;
  }
  .skills-bar-content p{
    font-size: 14px;
    font-weight: 700;
  }
  .sk-bar{
    width: 100%;
    height: 4px;
    border-radius: 5px;
    background-color: #E4E4E4;
    margin: 10px 0;
    overflow: hidden;
  }

  .sk-bar .sk-bar-step{
    height: 100%;
    width: 0;
    background-color: #ff9800;
    width: 49%;
  }

  .skills-bar-content i{
    position: absolute;
    top: -5px;
    left: 0;
    transition: all .5s;
  }

  /*.icon-1,.icon-2,.icon-3,.icon-4,.icon-5,.icon-6,.icon-7{
    width: 30px;
    height: 30px;
    background: url("../assets/biaoqing.png") no-repeat;
    display: block;
  }*/

  /*.icon-1{
    background-position: 0 0;
    background-size: 140px;
  }

  .icon-2{
    background-position: 0 -38px;
    background-size: 140px;
  }

  .icon-3{
    background-position: 0 -70px;
    background-size: 140px;
  }*/
</style>
