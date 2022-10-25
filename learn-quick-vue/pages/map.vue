<template>
    <div>
        <link
        href="https://cdn.jsdelivr.net/npm/tailwindcss@2.1.2/dist/tailwind.min.css"
        rel="stylesheet"
        />
        <NavBar />
        <l-map style="height: 92vh" :zoom="zoom" :center="center">
            <l-tile-layer :url="url" :attribution="attribution"></l-tile-layer>
            <l-marker :lat-lng="markerVannes"></l-marker>
            <l-marker :lat-lng="markerEvry"></l-marker>
        </l-map>
    </div>
  </template>
  
<script lang="ts">
    import Vue from 'vue'
    import { LMap, LTileLayer, LMarker } from 'vue2-leaflet';
    import { Icon } from 'leaflet';
    
    type D = Icon.Default & {
        _getIconUrl?: string;
    };

    delete (Icon.Default.prototype as D)._getIconUrl;
    Icon.Default.mergeOptions({
        iconRetinaUrl: require('leaflet/dist/images/marker-icon-2x.png'),
        iconUrl: require('leaflet/dist/images/marker-icon.png'),
        shadowUrl: require('leaflet/dist/images/marker-shadow.png'),
    });

    Vue.component('l-map', LMap);
    Vue.component('l-tile-layer', LTileLayer);
    Vue.component('l-marker', LMarker);

    export default Vue.extend({
        components: {
            LMap,
            LTileLayer,
            LMarker
        },
        data () {
            return {
                url: 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png',
                attribution:
                    '&copy; <a target="_blank" href="http://osm.org/copyright">OpenStreetMap</a> contributors',
                zoom: 15,
                center: [47.658, -2.760],
                markerVannes: [47.658, -2.760],
                markerEvry : [48.266,3.250]
            };
        }
    })
</script>

<style>
    @import "leaflet/dist/leaflet.css";
</style>