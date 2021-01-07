<template>
    <div class="container jumbotron">
        <a id="directions"><h2>Directions</h2></a>
        <div class="container">
            <GmapMap
            :center="{lat:-26.04, lng:28.07}"
            :zoom="17"
            map-type-id="terrain"
            style="width: 1000px; height: 500px;"
            >
            <GmapMarker
                :key="index"
                v-for="(m, index) in markers"
                :position="m.position"
                :clickable="true"
                :draggable="true"
                @click="center=m.position"
            />
            </GmapMap>
        </div>
        <p>Addtional Text and Directions</p>
    </div>
</template>
<script>
import * as VueGoogleMaps from 'vue2-google-maps';

export default {
  name: 'directions',
  data() {
    return {
      property: {
        lat: 1.28237,
        lng: 103.783098,
      },
      markers: {
        0: {
          full_name: 'Suite 22',
          position: {
            lat: '-26.03',
            lng: '28.06',
          },
        },
      },
    };
  },
  mounted() {
  },
  methods: {},
  computed: {
    google: VueGoogleMaps.gmapApi,
  },
};
</script>
