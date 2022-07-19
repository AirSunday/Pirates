<template>
<div class="parent">
  <div class="main">
    <Header></Header>
    <p><a name="aabout"></a></p> 
    <FirstInfo></FirstInfo>
    <p><a name="aroadmap"></a></p> 
    <Map></Map>
    <p><a name="afaq"></a></p> 
    <OpenList></OpenList>
    <p><a name="ateam"></a></p> 
    <Team></Team>
    <Board></Board>
  </div>
</div>
</template>

<script>
import Header from './components/Header.vue'
import FirstInfo from './components/FirstInfo.vue'
import Map from './components/Map.vue'
import OpenList from './components/OpenList.vue'
import Team from './components/Team.vue'
import Board from './components/Board.vue'

export default {
    name: "App",
    components: { Header, FirstInfo, Map, OpenList, Team, Board },
}
</script>

<style>
.main{
   margin: auto;
}
.parent{
    width: 100%;
    height: 100%;
    position: fixed;
    top: 0;
    left: 0;
    display: flex;
    overflow: auto;
}
</style>
