<template>
  <div id="app">
    <router-view></router-view>
    <router-view name="footer"></router-view>
  </div>
</template>

<script>
export default {
  name: 'App',
  mounted(){
    (function findDimensions(){
        var winHeight = 0;
        if (window.innerHeight)
        winHeight = window.innerHeight;
        else if ((document.body) && (document.body.clientHeight))
        winHeight = document.body.clientHeight;
        if (document.documentElement  && document.documentElement.clientHeight){
          winHeight = document.documentElement.clientHeight;
        }
        document.body.style.height = winHeight +'px';
        document.getElementById('app').style.height = winHeight +'px';
    }())
  }
}
</script>

<style>
body, h1, h2, h3, h4, h5, h6, hr, p, blockquote, dl, dt, dd, ul, ol, li, pre, form, fieldset, legend, button, input, textarea, th, td { margin: 0; padding: 0; } body, button, input, select, textarea { font: "Microsoft YaHei", tahoma, arial, \5b8b\4f53, Verdana, Simsun; -webkit-overflow-scrolling: touch; -webkit-tap-highlight-color: transparent; list-style: none; } h1, h2, h3, h4, h5, h6 { font-size: 100%; font-weight: normal; } address, cite, dfn, em, var { font-style: normal; } code, kbd, pre, samp { font-family: couriernew, courier, monospace; } small { font-size: 12px; } body { color: #191919; } ul, ol { list-style: none; } a { text-decoration: none; cursor: pointer; color: #666; } a:hover { text-decoration: none; } sup { vertical-align: text-top; } sub { vertical-align: text-bottom; } legend { color: #000; } img { vertical-align: middle; } fieldset, img { border: 0; vertical-align: top; } button, input, select, textarea { font-size: 100%; } table { border-collapse: collapse; border-spacing: 0; } input, button, select, textarea { outline: none; } textarea { resize: none; } /* 禁用了文本的拖拉，尤其在谷歌下 */ p { text-align: justify; text-justify: distribute; } /* 为了使文本段落左右两边对齐 */ /* 清除浮动 */ .clearfix:after { content: "."; display: block; height: 0; visibility: hidden; clear: both; } .clearfix { zoom: 1; } body, html { width: 100%; height: auto; overflow-x: hidden; padding: 0; margin: 0;  position: relative; } html { height: 100%; } body { font-size: .16rem; min-height: 100%; overflow-y: scroll; }
body,pre{
  font-family: Helvetica Neue,Helvetica,Arial,PingFang SC,Hiragino Sans GB,Heiti SC,Microsoft YaHei,WenQuanYi Micro Hei,sans-serif;
  margin:0;
}
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
[v-cloak]{
  display: none;
}
</style>
