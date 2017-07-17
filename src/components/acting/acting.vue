<template>
  <div class="actiing">
    <div class="actingCon">
      <transition name="move">
        <div class="imitate cutcircle">
          <div class="imitateImg"></div>
        </div>
      </transition>
      <p class="actingConp">正在加载</p>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
  export default{
    name:'acting'
  }
</script>

<style>
  @-moz-keyframes refreshing-loader {
    0% {
      -moz-transform: rotate(0deg);
      transform: rotate(0deg);
    }
    100% {
      -moz-transform: rotate(360deg);
      transform: rotate(360deg);
    }
  }
  @-webkit-keyframes refreshing-loader {
    0% {
      -webkit-transform: rotate(0deg);
      transform: rotate(0deg);
    }
    100% {
      -webkit-transform: rotate(360deg);
      transform: rotate(360deg);
    }
  }
  @keyframes refreshing-loader {
    0% {
      -moz-transform: rotate(0deg);
      -ms-transform: rotate(0deg);
      -webkit-transform: rotate(0deg);
      transform: rotate(0deg);
    }
    100% {
      -moz-transform: rotate(360deg);
      -ms-transform: rotate(360deg);
      -webkit-transform: rotate(360deg);
      transform: rotate(360deg);
    }
  }
  .actiing{
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    display: -webkit-flex;
    -webkit-justify-content: center;
    -webkit-align-items: center;
    background: rgba(0,0,0,0.6);
    z-index: 500;
  }
  .actingCon{
    padding: 2em 12px;
    width: 128px;
    border: none;
    border-radius: 10px;
    background: rgba(0,0,0,0.8);
    box-sizing: border-box;
    -webkit-box-sizing: border-box;
    box-sizing: border-box;
  }
  .actingCon>p{
    font-size: 14px;
    color: #fff;
    text-align: center;
    margin-top: 1em;
    word-break: break-all;
    word-wrap: break-word;
  }
  .imitate{
    position: relative;
    width: 50px;
    height: 50px;
    border-radius: 50%;
    -webkit-border-radius: 50%;
    -moz-border-radius: 50%;
    border: 0.24em solid #ffffff;
    margin: auto;
    box-sizing: border-box;
    -webkit-box-sizing: border-box;
    box-sizing: border-box;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .imitate.cutcircle{
    border-left-color: transparent;
    -moz-animation: refreshing-loader 800ms infinite linear;
    -webkit-animation: refreshing-loader 800ms infinite linear;
    animation: refreshing-loader 800ms infinite linear;
  }
  .imitateImg{
    width: 40px;
    height: 40px;
    border-radius: 50%;
    -webkit-border-radius: 50%;
    -moz-border-radius: 50%;
    box-sizing: border-box;
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    transform: scale(.6);
    -webkit-transform: scale(.6);
    -moz-transform: scale(.6);
    -ms-transform: scale(.6);
    -o-transform: scale(.6);
    -m-transform: scale(.6);
    -s-transform: scale(.6);
  }
  @media screen and (max-width:430px) and (orientation:portrait){
    .actingCon {
      transform: scale(0.9);
    }
  }
</style>
