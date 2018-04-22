<template>
  <div class="experience" id="Experience">
    <div class="gw">
      <div class="experience-tit"><h3>Work Experience</h3></div>
      <div class="w3-agile-experience-grids">
        <div class="experience-top-grids">
          <div class="experience-grid">
            <div class="experience-grid-icon icon-left hvr-radial-out">
              <i class="fa fa-folder-open" aria-hidden="true"></i>
            </div>
            <div class="experience-grid-info">
              <h5>Ut dapibus nisi turpis</h5>
              <p>Curabitur augue urna, venenatis vel enim at, sodales tempus diam. Aliquam ornare, magna a cursus tempus, arcu massa accumsan justo, non facilisis risus ante vel ex.</p>
            </div>
          </div>
          <div class="experience-grid experience-grid1">
            <div class="experience-grid-icon icon-left hvr-radial-out">
              <i class="fa fa-bell" aria-hidden="true"></i>
            </div>
            <div class="experience-grid-info">
              <h5>Ut dapibus nisi turpis</h5>
              <p>Curabitur augue urna, venenatis vel enim at, sodales tempus diam. Aliquam ornare, magna a cursus tempus, arcu massa accumsan justo, non facilisis risus ante vel ex.</p>
            </div>
          </div>
        </div>
        <div class="experience-top-grids">
          <div class="experience-grid experience-grid2">
            <div class="experience-grid-icon icon-left hvr-radial-out">
              <i class="fa fa-comments" aria-hidden="true"></i>
            </div>
            <div class="experience-grid-info">
              <h5>Ut dapibus nisi turpis</h5>
              <p>Curabitur augue urna, venenatis vel enim at, sodales tempus diam. Aliquam ornare, magna a cursus tempus, arcu massa accumsan justo, non facilisis risus ante vel ex.</p>
            </div>
          </div>
          <div class="experience-grid experience-grid3">
            <div class="experience-grid-icon icon-left hvr-radial-out">
              <i class="fa fa-asterisk" aria-hidden="true"></i>
            </div>
            <div class="experience-grid-info">
              <h5>Ut dapibus nisi turpis</h5>
              <p>Curabitur augue urna, venenatis vel enim at, sodales tempus diam. Aliquam ornare, magna a cursus tempus, arcu massa accumsan justo, non facilisis risus ante vel ex.</p>
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

      }
    }
  }
</script>

<style scoped>
  .experience{
    box-sizing: border-box;
    padding: 30px 0;
    background: url(../assets/s2.jpg) no-repeat 0px 0;
    background-size: cover;
  }

  .experience-tit h3{
    font-size: 2em;
    margin: 10px 0 30px;
    font-family: 'Roboto Slab', serif;
    font-weight: 700;
    letter-spacing: 1px;
    text-transform: uppercase;
    color: #ffffff;
  }
  .w3-agile-experience-grids {
    margin: 4em 0 0 0;
  }

  .experience-top-grids{
    display: flex;
    display: -webkit-flex;
    flex-direction: row;
    justify-content: space-between;
  }

  .experience-grid{
    text-align: center;
    padding: 2em;
    border-right: solid 1px #fff;
    border-bottom: solid 1px #fff;
  }

  .experience-grid-icon i.fa{
    box-sizing: border-box;
    color: #2f2f2f;
    background: white;
    border: solid 2px #ff9800;
    width: 100px;
    height: 100px;
    font-size: 2em;
    padding: 1.1em 0 0 0;
    transition: all .5s;
  }

  .experience-grid:hover div i.fa.fa-folder-open,.experience-grid:hover div i.fa.fa-bell,.experience-grid:hover div i.fa.fa-comments,.experience-grid:hover div i.fa.fa-asterisk{
    color: #fff;
    background: #ff9800;
    border-color: #fff;
    transform: rotate3d(360,360, 360 ,360deg);
  }

  .experience-grid-info h5{
    color: #fff;
    font-size: 1.5em;
    margin: 1em 0 0 0;
    font-weight: 700;
  }
  .experience-grid-info p{
    color: #fff;
    font-size: .9em;
    margin: 1em 0 0 0;
    line-height: 1.8em;
  }
  .experience-grid1 {
    border-right: none !important;
  }
  .experience-grid2 {
    border-bottom: none !important;
  }
  .experience-grid3 {
    border-bottom: none !important;
    border-right: none !important;
  }

</style>
