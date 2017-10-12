<template>
   <div class="map-container">
    <gmap-map id="gmap"
      :center="center"
      :zoom="13">

      <gmap-info-window 
        :options="infoOptions" 
        :position="infoWindowPos"
        :opened="infoWinOpen"
        @closeclick="infoWinOpen=false">
          <h1>{{ infoTitleContent }}</h1>
          <p>{{ infoDetailContent }}</p>
      </gmap-info-window>

      <gmap-marker
        :key="index"
        v-for="(m, index) in markers"
        :position="m.position"
        :clickable="true"
        :draggable="false"
        @click="infoAlert(m)">
      </gmap-marker>

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
        center: {
          lat: 40.7357, 
          lng: -74.1724
        },
        infoTitleContent: '',
        infoDetailContent: '',
        infoWindowPos: {
          lat: 0, 
          lng: 0
        },
        infoWinOpen: false,
        currentMidx: null,
        infoOptions: {
          pixelOffset: {
            width: 0,
            height: -35
          }
        },
        markers: [{
          position: {lat: 40.7357, lng: -74.1724},
          infoTitle: 'Program 1',
          infoDetail: 'Marker 1'
        }, {
          position: {lat: 40.727, lng: -74.170},
          infoTitle: 'Program 2',
          infoDetail: 'Marker 2'
        }, {
          position: {lat: 40.7321, lng: -74.1731},
          infoTitle: 'Program 3',
          infoDetail: 'Marker 3'  
        }]
      }
    },
    methods: {
      toggleInfoWindow: function(marker, idx) {
        this.infoWindowPos = marker.position;
        this.infoTitleContent = marker.infoTitle;
        this.infoDetailContent = marker.infoDetail;

        if (ths.currentMidx == idx) {
          this.infoWinOpen = !this.infoWinOpen;
        }
        else {
          this.infoWinOpen = true;
          this.currentMidx = idx;
        }
      },
      infoAlert: function(m) {
        alert("Temporary alert: " + m.infoDetail);
      }
    }
  }

</script>

<style>


    #gmap {
      width: 100%;
      height: 700px;
    }
</style>
