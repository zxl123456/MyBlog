<template>
    <div>
      <v-menu></v-menu>
      <v-banner></v-banner>
      <v-about-me></v-about-me>
      <v-experience></v-experience>
      <v-project></v-project>
      <v-contact-me></v-contact-me>
    </div>
</template>

<script>
    import VBanner from '../components/banner'
    import VMenu from '../components/menu'
    import VAboutMe from '../components/aboutMe'
    import VExperience from '../components/experience'
    import VProject from '../components/myProject'
    import VContactMe from '../components/contact'
    export default {
      data(){
        return{

        }
      },
      components:{
        VBanner,VMenu,VAboutMe,VExperience,VProject,VContactMe
      }
    }
</script>

<style>

  .gw{
    width: 1080px;
    min-width: 1080px;
    margin: 0 auto;
  }

  html, body, div, object, iframe,p,
  dl, dt, dd, ul, ol, li, h1, h2, h3, h4, h5, h6, p, blockquote, pre,
  fieldset, form, label, legend, button, input, textarea,
  table, caption, tbody, tfoot, thead, tr, th, td,
  a, abbr, address, acronym, cite, code, del, dfn, em, img, ins, kbd, q, span, samp, small, strike, strong, sub, sup, tt, var, b, u, i, center,
  section, article, aside, header, footer, nav, menu, hgroup, dialog, details, summary, figure, figcaption, canvas, embed, output, ruby, time, mark, audio, video {
    margin: 0;
    padding: 0;
    font-family: 'Roboto Condensed', sans-serif;
  }

  .hidden{
    display: none!important;
  }

  html {
    color: #333;
    background: #f5f5f5; }

  body {
    line-height: 1;
  }

  section, article, aside, header, footer, nav, menu, hgroup, dialog, details, figure, figcaption {
    display: block; }

  h1, h2, h3, h4, h5, h6 {
    font-size: 100%;
    font-weight: normal; }

  ul, ol, li {
    list-style: none; }

  table {
    border-collapse: collapse;
    border-spacing: 0; }

  caption, th {
    text-align: left; }

  fieldset, img {
    border: 0; }

  legend {
    color: #333; }

  input, textarea, select {
    font-family: 'Roboto Condensed', sans-serif;
    font-weight: inherit;
    font-size: inherit; }

  input, textarea, select {
    *font-size: 100%; }

  legend {
    color: #333; }

  address, caption, cite, code, dfn, em, th, var {
    font-style: normal;
    font-weight: normal; }

  blockquote:before, blockquote:after, q:before, q:after {
    content: ''; }

  sup {
    vertical-align: text-top; }

  sub {
    vertical-align: text-bottom; }

  a:link, a:visited {
    text-decoration: none; }

  a:hover, a:active, a:focus {
    text-decoration: none;
    outline: 0; }

  /* form element base style */
  input[type="radio"], input.radio, input[type="checkbox"], input.checkbox {
    margin-right: 3px;
    vertical-align: middle; }

  input[type="text"], input.text, input[type="password"], input.password {
    padding: 4px 10px;
    border: 1px solid #ccc; }
  input[type="text"]:hover, input[type="text"]:active, input[type="text"]:focus, input.text:hover, input.text:active, input.text:focus, input[type="password"]:hover, input[type="password"]:active, input[type="password"]:focus, input.password:hover, input.password:active, input.password:focus {
    border-color: #bbbbbb; }

  textarea {
    padding: 5px;
    border: 1px solid #ccc; }
  textarea:hover, textarea:active, textarea:focus {
    border-color: #bbbbbb; }

  select {
    padding: 0 3px;
    border: 1px solid #ccc; }
  select:hover, select:active, select:focus {
    border-color: #bbbbbb; }
  select optgroup {
    font-weight: 700;
    font-style: normal; }
  select option {
    font-weight: 400;
    font-style: normal; }

  /* base */
  .pr {
    position: relative; }

  .pa {
    position: absolute; }
  .fal{float:right;
    display: inline;

  }

  .fl {
    float: left; }
  .fr {
    float: right; }

  .cl {
    clear: left; }

  .cr {
    clear: right; }

  .cb {
    clear: both; }

  .bc {
    margin-left: 0;
    margin-right: 0; }

  .clear {
    height: 0;
    clear: both;
    font-size: 0;
    overflow: hidden;
    visibility: hidden; }

  .clearfix:before,.clearfix:after {
    content: "";
    display: block;
    clear: both;
  }
  .clearfix {
    zoom: 1;
  }
  .tl {
    text-align: left; }

  .tc {
    text-align: center; }

  .tr {
    text-align: right; }

  .vat {
    vertical-align: top; }

  .vam {
    vertical-align: middle; }

  .vab {
    vertical-align: bottom; }

  .hidden {
    display: none; }

  .vs {
    visibility: visible; }

  .vh {
    visibility: hidden; }

  .zoom {
    zoom: 1; }

  .w10 {
    width: 10px; }

  .w20 {
    width: 20px; }

  .w30 {
    width: 30px; }

  .w40 {
    width: 40px; }

  .w50 {
    width: 50px; }

  .w60 {
    width: 60px; }

  .w70 {
    width: 70px; }

  .w80 {
    width: 80px; }

  .w90 {
    width: 90px; }

  .w100 {
    width: 100px; }

  .w200 {
    width: 200px; }

  .w300 {
    width: 300px; }

  .w400 {
    width: 400px; }

  .w500 {
    width: 500px; }

  .w600 {
    width: 600px; }

  .w700 {
    width: 700px; }

  .w800 {
    width: 800px; }

  .w900 {
    width: 900px; }

  .w1000 {
    width: 1000px; }

  .w210 {
    width: 210px; }

  .w220 {
    width: 220px; }

  .w230 {
    width: 230px; }

  .w240 {
    width: 240px; }

  .w250 {
    width: 250px; }

  .w260 {
    width: 260px; }

  .w270 {
    width: 270px; }

  .w280 {
    width: 280px; }

  .w290 {
    width: 290px; }

  .w300 {
    width: 300px; }

  .w310 {
    width: 310px; }

  .w320 {
    width: 320px; }

  .w330 {
    width: 330px; }

  .w340 {
    width: 340px; }

  .w350 {
    width: 350px; }

  .w360 {
    width: 360px; }

  .w370 {
    width: 370px; }

  .w380 {
    width: 380px; }

  .w390 {
    width: 390px; }

  .h30 {
    height: 30px; }

  .h50 {
    height: 50px; }

  .h80 {
    height: 80px; }

  .h100 {
    height: 100px; }

  .h200 {
    height: 200px; }

  .minH300 {
    min-height: 300px;
    _height: 300px; }

  .minH400 {
    min-height: 400px;
    _height: 400px; }

  .minH500 {
    min-height: 500px;
    _height: 500px; }

  .minH600 {
    min-height: 600px;
    _height: 600px; }

  .minH700 {
    min-height: 700px;
    _height: 700px; }

  .minH800 {
    min-height: 800px;
    _height: 800px; }

  .wone {
    width: 100%; }

  .hone {
    height: 100%; }

  .blank, .blank3, .blank5, .blank6, .blank9, .blank10, .blank15, .blank20, .blank30 {
    display: block;
    overflow: hidden;
    clear: both; }

  .blank3 {
    height: 3px; }

  .blank5 {
    height: 5px; }

  .blank6 {
    height: 6px; }

  .blank9 {
    height: 9px; }

  .blank10 {
    height: 10px; }

  .blank15 {
    height: 15px; }

  .blank20 {
    height: 20px; }

  .blank30 {
    height: 30px; }

  .m5 {
    margin: 5px; }

  .mt5 {
    margin-top: 5px; }

  .mb5 {
    margin-bottom: 5px; }

  .mtb5 {
    margin-top: 5px;
    margin-bottom: 5px; }

  .ml5 {
    margin-left: 5px; }

  .mr5 {
    margin-right: 5px; }

  .mlr5 {
    margin-left: 5px;
    margin-right: 5px; }

  .m10 {
    margin: 10px; }

  .mt10 {
    margin-top: 10px; }

  .mb10 {
    margin-bottom: 10px; }

  .mtb10 {
    margin-top: 10px;
    margin-bottom: 10px; }

  .ml10 {
    margin-left: 10px; }

  .mr10 {
    margin-right: 10px; }

  .mlr10 {
    margin-left: 10px;
    margin-right: 10px; }

  .m15 {
    margin: 15px; }

  .mt15 {
    margin-top: 15px; }

  .mb15 {
    margin-bottom: 15px; }

  .mtb15 {
    margin-top: 15px;
    margin-bottom: 15px; }

  .ml15 {
    margin-left: 15px; }

  .mr15 {
    margin-right: 15px; }

  .mlr15 {
    margin-left: 15px;
    margin-right: 15px; }

  .m20 {
    margin: 20px; }

  .mt20 {
    margin-top: 20px; }

  .mb20 {
    margin-bottom: 20px; }

  .mtb20 {
    margin-top: 20px;
    margin-bottom: 20px; }

  .ml20 {
    margin-left: 20px; }

  .mr20 {
    margin-right: 20px; }

  .mlr20 {
    margin-left: 20px;
    margin-right: 20px; }

  .m30 {
    margin: 30px; }

  .mt30 {
    margin-top: 30px; }

  .mb30 {
    margin-bottom: 30px; }

  .mtb30 {
    margin-top: 30px;
    margin-bottom: 30px; }

  .ml30 {
    margin-left: 30px; }

  .mr30 {
    margin-right: 30px; }

  .mlr30 {
    margin-left: 30px;
    margin-right: 30px; }

  .m40 {
    margin: 40px; }

  .mt40 {
    margin-top: 40px; }

  .mb40 {
    margin-bottom: 40px; }

  .mtb40 {
    margin-top: 40px;
    margin-bottom: 40px; }

  .ml40 {
    margin-left: 40px; }

  .mr40 {
    margin-right: 40px; }

  .mlr40 {
    margin-left: 40px;
    margin-right: 40px; }

  .m50 {
    margin: 50px; }

  .mt50 {
    margin-top: 50px; }

  .mb50 {
    margin-bottom: 50px; }

  .mtb50 {
    margin-top: 50px;
    margin-bottom: 50px; }

  .ml50 {
    margin-left: 50px; }

  .mr50 {
    margin-right: 50px; }

  .mlr50 {
    margin-left: 50px;
    margin-right: 50px; }

  .m80 {
    margin: 80px; }

  .mt80 {
    margin-top: 80px; }

  .mb80 {
    margin-bottom: 80px; }

  .mtb80 {
    margin-top: 80px;
    margin-bottom: 80px; }

  .ml80 {
    margin-left: 80px; }

  .mr80 {
    margin-right: 80px; }

  .mlr80 {
    margin-left: 80px;
    margin-right: 80px; }

  .m100 {
    margin: 100px; }

  .mt100 {
    margin-top: 100px; }

  .mb100 {
    margin-bottom: 100px; }

  .mtb100 {
    margin-top: 100px;
    margin-bottom: 100px; }

  .ml100 {
    margin-left: 100px; }

  .mr100 {
    margin-right: 100px; }

  .mlr100 {
    margin-left: 100px;
    margin-right: 100px; }

  .p5 {
    padding: 5px; }

  .pt5 {
    padding-top: 5px; }

  .pb5 {
    padding-bottom: 5px; }

  .ptb5 {
    padding-top: 5px;
    padding-bottom: 5px; }

  .pl5 {
    padding-left: 5px; }

  .pr5 {
    padding-right: 5px; }

  .plr5 {
    padding-left: 5px;
    padding-right: 5px; }

  .p10 {
    padding: 10px; }

  .pt10 {
    padding-top: 10px; }

  .pb10 {
    padding-bottom: 10px; }

  .ptb10 {
    padding-top: 10px;
    padding-bottom: 10px; }

  .pl10 {
    padding-left: 10px; }

  .pr10 {
    padding-right: 10px; }

  .plr10 {
    padding-left: 10px;
    padding-right: 10px; }

  .p15 {
    padding: 15px; }

  .pt15 {
    padding-top: 15px; }

  .pb15 {
    padding-bottom: 15px; }

  .ptb15 {
    padding-top: 15px;
    padding-bottom: 15px; }

  .pl15 {
    padding-left: 15px; }

  .pr15 {
    padding-right: 15px; }

  .plr15 {
    padding-left: 15px;
    padding-right: 15px; }

  .p20 {
    padding: 20px; }

  .pt20 {
    padding-top: 20px; }

  .pb20 {
    padding-bottom: 20px; }

  .ptb20 {
    padding-top: 20px;
    padding-bottom: 20px; }

  .pl20 {
    padding-left: 20px; }

  .pr20 {
    padding-right: 20px; }

  .plr20 {
    padding-left: 20px;
    padding-right: 20px; }

  .p30 {
    padding: 30px; }

  .pt30 {
    padding-top: 30px; }

  .pb30 {
    padding-bottom: 30px; }

  .ptb30 {
    padding-top: 30px;
    padding-bottom: 30px; }

  .pl30 {
    padding-left: 30px; }

  .pr30 {
    padding-right: 30px; }

  .plr30 {
    padding-left: 30px;
    padding-right: 30px; }

  .p50 {
    padding: 50px; }

  .pt50 {
    padding-top: 50px; }

  .pb50 {
    padding-bottom: 50px; }

  .ptb50 {
    padding-top: 50px;
    padding-bottom: 50px; }

  .pl50 {
    padding-left: 50px; }

  .pr50 {
    padding-right: 50px; }

  .plr50 {
    padding-left: 50px;
    padding-right: 50px; }

  .p100 {
    padding: 100px; }

  .pt100 {
    padding-top: 100px; }

  .pb100 {
    padding-bottom: 100px; }

  .ptb100 {
    padding-top: 100px;
    padding-bottom: 100px; }

  .pl100 {
    padding-left: 100px; }

  .pr100 {
    padding-right: 100px; }

  .plr100 {
    padding-left: 100px;
    padding-right: 100px; }

  .pl300 {
    padding-left: 300px; }

  .pl400 {
    padding-left: 400px; }

  .fs10 {
    font-size: 10px; }

  .fs11 {
    font-size: 11px; }

  .fs12 {
    font-size: 12px; }

  .fs13 {
    font-size: 13px; }

  .fs14 {
    font-size: 14px; }

  .fs15 {
    font-size: 15px; }

  .fs16 {
    font-size: 16px; }

  .fs18 {
    font-size: 18px; }

  .fs20 {
    font-size: 20px; }

  .fs22 {
    font-size: 22px; }

  .fs24 {
    font-size: 24px; }

  .fs26 {
    font-size: 26px; }

  .fs28 {
    font-size: 28px; }

  .fs30 {
    font-size: 30px; }

  .fs36 {
    font-size: 36px; }

  .fs40 {
    font-size: 40px; }

  .fw400 {
    font-weight: 400; }

  .fw700 {
    font-weight: 700; }

  .fwn {
    font-weight: normal; }

  .fwb {
    font-weight: bold; }

  .lh18 {
    line-height: 18px; }

  .lh20 {
    line-height: 20px; }

  .lh22 {
    line-height: 22px; }

  .lh24 {
    line-height: 24px; }

  .lh26 {
    line-height: 26px; }

  .lh28 {
    line-height: 28px; }

  .lh30 {
    line-height: 30px; }

  .lh40 {
    line-height: 40px; }

  .lh50 {
    line-height: 50px; }

  .lh100 {
    line-height: 100%; }

  .lh150 {
    line-height: 150%; }

  .lh180 {
    line-height: 180%; }

  .lh200 {
    line-height: 200%; }

  .ti2 {
    text-indent: 2em; }

  .tdu {
    text-decoration: underline; }

  .tdn {
    text-decoration: none; }

  .wb {
    word-wrap: break-word;
    word-break: break-all; }

  .text-3row{
    overflow : hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 3;
    -webkit-box-orient: vertical;
  }
  .clearfix:after{
    display: block;
    clear: both;
    content: "";
    visibility: hidden;
    height: 0;
  }
  .clearfix{
    zoom:1;
  }
  .banner-right-button{
    margin-top: 30px;
    width: 100%;
    float: left;
    text-align: left;
    margin-bottom: 50px;
  }

  .banner-right-button a {
    padding: .5em 2em;
    color: #ffffff !important;
    text-transform: uppercase;
    background: #FF9800;
    font-weight: 700 !important;
    text-decoration: none !important;
    line-height: initial !important;
    font-size: .9em !important;
    margin: 0 !important;
  }

  .banner-right-button a:focus{
    outline:none;
  }

  .hvr-sweep-to-bottom {
    display: inline-block;
    vertical-align: middle;
    -webkit-transform: translateZ(0);
    transform: translateZ(0);
    box-shadow: 0 0 1px rgba(0, 0, 0, 0);
    -webkit-backface-visibility: hidden;
    backface-visibility: hidden;
    -moz-osx-font-smoothing: grayscale;
    position: relative;
    -webkit-transition-property: color;
    transition-property: color;
    -webkit-transition-duration: 0.3s;
    transition-duration: 0.3s;
  }
  .hvr-sweep-to-bottom:before {
    content: "";
    position: absolute;
    z-index: -1;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: #ffffff;
    -webkit-transform: scaleY(0);
    transform: scaleY(0);
    -webkit-transform-origin: 50% 0;
    transform-origin: 50% 0;
    -webkit-transition-property: transform;
    transition-property: transform;
    -webkit-transition-duration: 0.3s;
    transition-duration: 0.3s;
    -webkit-transition-timing-function: ease-out;
    transition-timing-function: ease-out;
  }
  .hvr-sweep-to-bottom:hover, .hvr-sweep-to-bottom:focus, .hvr-sweep-to-bottom:active {
    color: #2f2f2f !important;
  }
  .hvr-sweep-to-bottom:hover:before, .hvr-sweep-to-bottom:focus:before, .hvr-sweep-to-bottom:active:before {
    -webkit-transform: scaleY(1);
    transform: scaleY(1);
  }

</style>
