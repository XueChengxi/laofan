<template>
  <div class="hello">
      <button @click = "Btn">
        点我
      </button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      
    }
  },
  methods : {
    Btn () {
      console.log('hahah')
      this.$router.push ({path : "/index",
      query : {
        id : Math.floor(Math.random()*10),
        name : "nihao"
      }})
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
