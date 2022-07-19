<template>
<div class="parentMap">  
<div class="maps" v-if="width > 650">
    <img class="pt1" src="../assets/imgs/roadmapBig/pt1.png"/>
    <table style="border:none">
        <tr>
            <td>
                <img class="pt23" src="../assets/imgs/roadmapBig/pt3.png"/>
            </td>
            <td>
                <img class="pt23" src="../assets/imgs/roadmapBig/pt2.png"/>
            </td>
        </tr>
    </table>
</div>
<div class="mapsMini" v-else>
    <img class="pt" src="../assets/imgs/roadmapMini/pt11.png"/>
    <img class="pt" src="../assets/imgs/roadmapMini/pt12.png"/>
    <img class="pt" src="../assets/imgs/roadmapMini/pt2.png"/>
    <img class="pt" src="../assets/imgs/roadmapMini/pt3.png"/>
</div>
</div>
</template>

<script>
export default {
    name: 'Map',
    data() {
        return {
            width: window.innerWidth,
        };
    },
    methods: {
        updateWidth() {
            this.width = window.innerWidth;
        },
    },
    created() {
        window.addEventListener("resize", this.updateWidth);
    },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.mapsMini{
    width: 60%;
    margin: 0 auto;
    resize: both;
}
.maps{
    width: 90%;
    margin: 0 auto;
    resize: both;
}
.parentMap{
    width: 90%;
    margin: 0 auto;
    resize: both;
}
.pt1{
    width: 100%;
    height: auto;
    max-width: 2000px;
}
.pt23{
    width: 100%;
    height: auto;
    max-width: 1000px;
}
.pt{
    width: 100%;
    height: auto;
    max-width: 300px;
}
</style>
