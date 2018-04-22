<template>
  <div class="contact" id="contact">
    <div class="container">
      <div class=" experience-heading">
        <h3>Contact Me</h3>
      </div>
      <div class="contact-form gw">
        <form action="#" method="post">
          <div class="fields-grid">
            <div class="styled-input agile-styled-input-top">
              <input type="text" name="Full Name" required="">
              <label>Full Name</label>
              <span></span>
            </div>
            <div class="styled-input agile-styled-input-top" style="float:right;">
              <input type="text" name="Phone" required="">
              <label>Phone</label>
              <span></span>
            </div>
            <div class="styled-input">
              <input type="text" name="Email" required="">
              <label>Email</label>
              <span></span>
            </div>
            <div class="styled-input" style="float:right;">
              <input type="text" name="Subject" required="">
              <label>Subject</label>
              <span></span>
            </div>
            <div class="clearfix"> </div>
          </div>
          <div class="styled-input textarea-grid">
            <textarea name="Message" required=""></textarea>
            <label>Message</label>
            <span></span>
          </div>
          <input type="submit" value="SEND">
        </form>
      </div>
    </div>
  </div>
</template>

<script>
    export default {
        name: "contact"
    }
</script>

<style scoped>

  .contact{
    box-sizing: border-box;
    padding: 40px 0 60px;
    background: url(../assets/3.jpg) no-repeat 0px 0;
    background-size: cover;
  }

  .experience-heading h3{
    font-size: 2em;
    margin: 10px 0 30px;
    font-family: 'Roboto Slab', serif;
    font-weight: 700;
    letter-spacing: 1px;
    text-transform: uppercase;
    color: #ffffff;
  }

  .styled-input.agile-styled-input-top {
    margin-top: 0;
  }
  .contact input[type="text"],.contact textarea{
    font-size: .9em;
    color: #ffffff;
    padding: 0.5em 1em;
    border: 0;
    width: 95%;
    border-bottom: 1px solid #dcdcdc;
    background: none;
    -webkit-appearance: none;
    outline: none;
  }
  .contact textarea {
    min-height: 150px;
    resize: none;
    width: 97%;
  }

  .styled-input input:focus ~ label, .styled-input input:valid ~ label,
  .styled-input textarea:valid ~ label,.styled-input textarea:focus ~ label {
    font-size: .9em;
    color: #333333;
    top: -1.3em;
    -webkit-transition: all 0.125s;
    -moz-transition: all 0.125s;
    -o-transition: all 0.125s;
    -ms-transition: all 0.125s;
    transition: all 0.125s;
  }
  .styled-input {
    width: 49%;
    margin: 2em 0 1em 1.5%;
    position: relative;
    float: left;
  }
  .styled-input:nth-child(1),.styled-input:nth-child(3){
    margin-left:0;
  }
  .textarea-grid{
    float:none !important;
    width:100% !important;
    margin-left:0 !important;
  }
  .styled-input label {
    color: #ffffff;
    padding: 0.5em .9em;
    position: absolute;
    top: 0;
    left: 0;
    -webkit-transition: all 0.3s;
    -moz-transition: all 0.3s;
    transition: all 0.3s;
    pointer-events: none;
    font-weight: 400;
    font-size: .9em;
    display: block;
    line-height: 1em;
  }
  .styled-input input ~ span,.styled-input textarea ~ span {
    display: block;
    width: 0;
    height: 2px;
    background: #ffffff;
    position: absolute;
    bottom: 0;
    left: 0;
    -webkit-transition: all 0.125s;
    -moz-transition: all 0.125s;
    transition: all 0.125s;
  }
  .styled-input textarea ~ span {
    bottom: 5px;
  }
  .styled-input input:focus.styled-input textarea:focus {
    outline: 0;
  }
  .styled-input input:focus ~ span,.styled-input textarea:focus ~ span {
    width: 100%;
    -webkit-transition: all 0.075s;
    -moz-transition: all 0.075s;
    transition: all 0.075s;
  }
  /*-- //input-effect --*/
  .contact input[type="submit"] {
    outline: none;
    color: #FFFFFF;
    padding: .5em 3em;
    font-size: .9em;
    font-weight: 600;
    margin: 1em 0 0 0;
    -webkit-appearance: none;
    background: #FF9800;
    border: 2px solid #ff9800;
    -webkit-transition: 0.5s all;
    -moz-transition: 0.5s all;
    -o-transition: 0.5s all;
    -ms-transition: 0.5s all;
    transition: 0.5s all;
    cursor: pointer;
  }
  .contact input[type="submit"]:hover {
    background-color: #ffffff;
    color: #333333;
    background:#ffffff;
    border: 2px solid #ffffff;
  }
</style>
