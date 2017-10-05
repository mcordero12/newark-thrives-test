<template>
   <div class="map-container">
    <gmap-map id="gmap"
      :center="center"
      :zoom="12"
    >
      <gmap-marker
        :key="index"
        v-for="(m, index) in markers"
        :position="m.position"
        :clickable="true"
        :draggable="true"
        @click="center=m.position"
      ></gmap-marker>
    </gmap-map>
  </div> 
</template>

<script>
  /////////////////////////////////////////
  // New in 0.4.0
  import * as VueGoogleMaps from 'vue2-google-maps';
  import Vue from 'vue';

  Vue.use(VueGoogleMaps, {
    load: {
      key: 'AIzaSyC_j4NpmLz1JmbXeEyjtW6S71fhhtVZaNk'
      // libraries: 'places', //// If you need to use place input
    }
  });

  export default {
    data () {
      return {
        center: {lat: 40.7357, lng: -74.1724},
        markers: [{
          position: {lat: 40.7357, lng: -74.1724}
        }, {
          position: {lat: 40.727, lng: -74.170}
        }, {
          position: {lat: 40.7321, lng: -74.1731}  
        }]
      }
    }
  }
</script>

<style>
    .map-container {
        width: 100%;
        height: 700px;
    }

    #gmap {
        width: 100%;
        height: 100%;
    }
</style>
