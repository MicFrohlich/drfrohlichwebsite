<template>
    <div class="container jumbotron">
        <h2 class="text-center"><u>Directions</u></h2>
        <div class="container">
            <GmapMap
            :center="{lat:-26.038, lng:28.07}"
            :zoom="17"
            map-type-id="terrain"
            class="box"
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
            <hr>
        <div class="d-flex justify-content-center">
          <a href="https://goo.gl/maps/ccJngo5UtjuLoJ4n6">Direct Me!</a>
        </div>
        </div>
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
            lat: -26.03,
            lng: 28.06,
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
