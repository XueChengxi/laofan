<template>
    <div class="hello">
        <h1>首页</h1>
        <h1 v-for = "(key,value,index) in URLList">{{value}} == {{key}} == {{index}}</h1>
        <h1>{{MM}}</h1>
        <h1>{{mm}}</h1>
    </div>
  </template>
  
  <script>
  export default {
    data () {
      return {
        URLList : {},
        MM : 0,
        mm : 0
      }
    },
    mounted () {
        // alert ('我是首页组件呀')
        // 获取url 地址以 ？形式传递的参数
        console.log(this.$route.query);
        console.log(this.$route.query.id)
        console.log(this.$route.query.name)
        this.URLList = this.$route.query;
        const aa = this;

        setInterval (function () {
            // 首先获取到10 以内的随机数  然后去除小数点
            aa.MM = (Math.random()*10).toFixed(0)
        },100)
    }
  }
  </script>
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
  
  </style>
  