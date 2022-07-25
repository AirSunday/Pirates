<template>  
  <div>
    <div v-if="width > 650" class="headerHide"></div>
    <div v-else class="headerHideSmall"></div>
    <header v-if="width > 650" class="header bigHeader">
      <img class="backGroundTitle" src="../assets/imgs/header/longHeader.png"/>
      <table class="tableHeader">
        <td><img class="title" src="../assets/imgs/header/title.png"></td>
        <td>
          <table id="listBoard">
            <td v-for="(el, key) in bord" :key="key">
              <a :href="'#a' + el" >
                <img class="board" :src="require(`../assets/imgs/header/${el}.png`)">
              </a>
            </td>
          </table>
        </td>
      </table>
    </header>
    <div v-else class="header smallHeader">
        <img @click="ShowBords" class="titleShort" style="z-index: 6;" src="../assets/imgs/header/titleSmall.png"><br>
        <div v-if="showBordsTrueFalse == true">
          <a href="#aabout">
            <img class="boardShort" style="z-index: 5;" :src="require(`../assets/imgs/shortHeader/about.png`)"><br>
          </a>
          <a href="#aroadmap">
            <img class="boardShort" style="z-index: 4;" :src="require(`../assets/imgs/shortHeader/roadmap.png`)"><br>
          </a>
          <a href="#afaq">
            <img class="boardShort" style="z-index: 3;" :src="require(`../assets/imgs/shortHeader/faq.png`)"><br>
          </a>
          <a href="#ateam">
            <img class="boardShort" style="z-index: 2;" :src="require(`../assets/imgs/shortHeader/team.png`)"><br>
          </a>
            <img class="boardShort" style="z-index: 1;" :src="require(`../assets/imgs/shortHeader/connectWallet.png`)">
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
  data() {
        return {
            bord: ["about", "roadmap", "faq", "team", "connectWallet"],
            width: window.innerWidth,
            showBordsTrueFalse: false,
        };
    },
    methods: {
        updateWidth() {
            this.width = window.innerWidth;
        },
        ShowBords() {
            this.showBordsTrueFalse = !this.showBordsTrueFalse;
        }
    },
    created() {
        window.addEventListener("resize", this.updateWidth);
    },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.headerHide{
  height: 100px;
}
.headerHideSmall{
  height: 50px;
}
.title {
  bottom: 0;
  width: 100%;
  max-width: 220px;
  height: auto;
}
.backGroundTitle{
  /* margin-top: 30px; */
  width: auto;
  height: 150%;
  max-height: 200px;
  position: absolute;
  z-index: -1;
}
.bigHeader{
  /* background: url(../assets/imgs/header/longHeader.png); */
}

.smallHeader{
  height: 70px;
  /* background: url(../assets/imgs/shortHeader/smallHeader.png); */
}

.header {
  /* background: url(./assets/imgs/header/longHeader.png); */
  position: fixed;
  padding: 0;
  margin: 0;
  top: -20px;
  left: 0;
  width: 100%;
  max-height: 100px;
}
.board {
  width: 100%;
  max-width: 170px;
  height: auto;
}
.tableHeader{
  margin-top: 5px;
  width: 100%;
  height: auto;
}
#listBoard {
  margin: auto 0 auto auto;
}
.titleShort{
  margin-top: 25px;
  margin-left: 10px;
  width: 100%;
  max-width: 140px;
  position: relative;
}
.boardShort{
  width: 100%;
  max-width: 130px;
  height: auto;
  margin-top: -40px;
  margin-left: 15px;
  position: relative;
}
.boardShortDiv{
  /* position:relative; */
}
</style>
