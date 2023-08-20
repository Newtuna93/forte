<template>
  <div>
        <h2>카카오맵 API 구현</h2>
        <div id="map"></div>
    </div>
</template>
<style scope>
    #map {
        width: 100%;
        height: 400px;
    }
</style>
<script>
    export default {
        name: "kakaoMap",
        data() {
            return {
                map: null
            };
        },
        setup() {

        },
        mounted() {
            if (window.kakao && window.kakao.maps) {
                this.loadMap();
            } else {
                this.loadScript();
            }
        },
        methods: {
            loadScript() {
                const script = document.createElement("script");
                script.type = "text/javascript"
                script.src = 
                    "//dapi.kakao.com/v2/maps/sdk.js?appkey=d9934f021be09a9f0a3630391607fbb8&autoload=false";
                script.onload = () => window.kakao.maps.load(this.loadMap);

                document.head.appendChild(script);
            },
            loadMap() {
                const container = document.getElementById("map");
                const option = {
                    center: new window.kakao.maps.LatLng(33.450701, 126.570667),
                    level: 3
                };

                this.map = new window.kakao.maps.Map(container, option);
            }
        }
    }
</script>