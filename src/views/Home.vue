<template>
  <div class="home">
    <button @click="test">test</button>
    <button @click="Bluetooth_status">Bluetooth_status</button>
    <button @click="writePermission">writePermission</button>
    <button @click="locationPermission">locationPermission</button>
    
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
      )
    },
    Bluetooth_status(){
      CosmosBeaconCordovaPlugin.isBluetoothEnabled(res=>{
        console.log("藍芽狀態：",res);
      })
    },
    writePermission(){
      CosmosBeaconCordovaPlugin.CheckWriteStoragePermission(res=>{
        console.log("寫外部空間權限：",res);
      })
    },
    locationPermission(){
      CosmosBeaconCordovaPlugin.CheckLocationPermission(res=>{
        console.log("位置權限：",res);
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
