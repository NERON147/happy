<template>
  <div id="app">
    <div class="svg">
<img src="@/assets/img/loyalty.svg" alt=""  class="flag">
  <svg id="progressCircle" width=200 height=200>
    <circle class="circle" cy=100 cx=100 r=80 fill="transparent" stroke="#ECECEC" stroke-width="7" stroke-dasharray="0,70,700" transform="rotate(-115 100 100)"></circle>
    <circle class="progress circle" cy=100 cx=100 r=80 fill="transparent" stroke="#70A84B" stroke-width="9" stroke-dasharray="0,1000" transform="rotate(-320 100 100)"></circle>
    <circle class="progress circle" cy=100 cx=100 r=80 fill="transparent" stroke="#FBD333" stroke-width="9" stroke-dasharray="0,1000" transform="rotate(-70 100 100)"></circle>
</svg>
  <div class="text-wrapper">
    <div class="proc-wrapper">
      <span class="proc">72<span class="dot">.</span></span>
  <span class="colproc">
    <span class="symbolproc">%</span>
    <span class="seven">7</span>
  </span>
    </div>
    <span class="loyal">Лояльность</span>
       <div><span class="downmiddle">ниже среднего</span></div>
    <div class="last-wrapper">
    <span class="minielem">по отрасли: FMCG</span>
    <span class="minielem">значений слева от медианы</span>
    <span class="rangeproc">52.0% - 83.1%</span>
    </div>
    <div class="lastcircleelem"> 
      <img class="treug"  src="@/assets/img/treug.svg" alt="">
    <span class="three">3.1</span>
    </div>
  </div>
    <img class="line" src="@/assets/img/line.svg" alt="">
    <div class="stat-wrapper">
      <div class="stat-text">Промоутеры</div>
      <div class="people-poc"> 
        <div class="count-proc">32.0%</div>
        <div class="peoplecount">
        <span class="countpeople">81</span>
        <img class="human" src="@/assets/img/human_full.svg" alt="">
        </div>
      </div>
      <div class="stat-graph">
         <span class="graph-proc"> +1,2%</span>
        <svg  width="56" height="20px">
  <rect id="progressGraph2" x="0" y="16"  width="0" height="6"  fill="#B5D0A2"  stroke-width="0"/>
  <rect id="progressGraph" x="0" y="0" width="0" height="16"  fill="#70A74B"  stroke-width="0"/>
</svg>
      </div>
      
    </div>
    <div class="stat-wrapper2">
      <div class="stat-text2">Скептики</div>
      <div class="people-poc"> 
        <div class="count-proc">39.1%</div>
        <div class="peoplecount">
        <span class="countpeople">8</span>
        <img class="human" src="@/assets/img/human_full.svg" alt="">
        </div>
      </div>
      <div class="stat-graph">
         <span class="graph-proc"> +4.8%</span>
        <svg  width="56" height="20px">
  <rect id="progressGraph2" x="0" y="16"  width="0" height="6"  fill="#FAE691"  stroke-width="0"/>
  <rect id="progressGraph5" x="0" y="0" width="0" height="16"  fill="#FAD233"  stroke-width="0"/>
</svg>
      </div>
      
    </div>
    <div class="stat-wrapper2">
      <div class="stat-text3">Критики</div>
      <div class="people-poc"> 
        <div class="count-proc">79.8%</div>
        <div class="peoplecount">
        <span class="countpeople">7</span>
        <img class="human" src="@/assets/img/human_full.svg" alt="">
        </div>
      </div>
      <div class="stat-graph">
         <span class="graph-proc"> -9.7%</span>
        <svg  width="56" height="20px">
  <rect id="progressGraph3" x="0" y="16"  width="0" height="6"  fill="#F1A69E"  stroke-width="0"/>
  <rect id="progressGraph4" x="0" y="0" width="0" height="16"  fill="#EA5243"  stroke-width="0"/>
</svg>
      </div>
      
    </div>
</div>
    
    
    
  </div>
</template>

<script>
export default {
  mounted () {
    function setProgress(progressCircle, val) {
  let el = document.getElementById(progressCircle);
  let circleProgressEl = el.children[0];
  let progressEl = el.children[2];
  let maxLength = circleProgressEl.getTotalLength();
  let progressLength = maxLength * val;
  progressEl.setAttribute('stroke-dasharray', progressLength + ',' + (maxLength  - progressLength));
}

function setProgress2(progressCircle, val) {
  let el = document.getElementById(progressCircle);
  let circleProgressEl = el.children[0];
  let progressEl2 = el.children[1];
  let maxLength = circleProgressEl.getTotalLength();
  let progressLength = maxLength * val;
  progressEl2.setAttribute('stroke-dasharray',  progressLength + ',' + (maxLength  - progressLength));
}

setProgress('progressCircle', .30);

setTimeout(function() {
  setProgress2('progressCircle', .30);
}, 800);
  }
}
</script>

<style>

</style>
