<template>
  <div class="home">
    <button @click="test">test</button>
  </div>
</template>

<script>
// @ is an alias to /src
/*eslint no-console:off */
export default {
  name: 'home',
  components: {
    HelloWorld
  },
  methods:{
    test(){
      console.log("進入")
    }
  }
}
</script>

<style  scoped>
button{
  width: 40px;
  height: 40px;
}
</style>
