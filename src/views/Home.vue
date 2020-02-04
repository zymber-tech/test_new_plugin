<template>
  <div class="home">
    <button @click="test">test</button>
  </div>
</template>

<script>
/* global CosmosBeaconCordovaPlugin */
/*eslint no-console:off */
export default {
  name: "home",
  methods: {
    test() {
      console.log("進入");
      CosmosBeaconCordovaPlugin.echo("太棒了!");
      CosmosBeaconCordovaPlugin.getDate(
        res => {
          console.log("現在時間：", res);
        },
        err => {
          console.log(err);
        }
      );
      CosmosBeaconCordovaPlugin.startScan(res=>{
        console.log("藍芽狀態：",res)
      })
    }
  }
};
</script>

<style  scoped>
button {
  width: 150px;
  height: 150px;
}
</style>
