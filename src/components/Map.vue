<template>
  <div id="map" class="map"></div>
</template>

<script>
import L from "leaflet";

export default {
  mounted() {
    var map = L.map("map").setView([61.254, 73.397], 13);

    L.tileLayer("https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png", {
      attribution:
        '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors',
    }).addTo(map);
  },
};
</script>

<style>
#map {
  width: 100%;
  height: 100vh;
}
</style>
