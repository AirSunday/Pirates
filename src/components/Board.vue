<template> 
<div class="mainBoard">
 <img class="board" :src="require(`../assets/imgs/board/board.png`)"/>
    <table class="elements">
        <td>
            <a href="https://discord.gg/3W3hfJb4"><img class="element" :src="require(`../assets/imgs/board/discord.png`)"/></a>
        </td>
        <td>
            <a href="https://twitter.com/pirates_nft?s=11"><img class="element" :src="require(`../assets/imgs/board/twitter.png`)"/></a>
        </td>
        <td>
            <a href="https://opensea.io/"><img class="element" :src="require(`../assets/imgs/board/opensea.png`)"/></a>
        </td>
    </table>
    <div class="hideBoard"></div>
</div>
</template>

<script>
export default {
    name: 'Team',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.board{
    width: 60%;
    height: auto;
    max-width: 1050px;
    position: absolute;
    z-index: -1;
}
.element{

    width: 60%;
    height: auto;
}
.elements{
    width: auto;
    height: auto;
    padding-top: 2%;
    padding-left: 12%;
    /* position: absolute; */
}
.mainBoard{
    width: 60%;
    margin: 0 auto;
    resize: both;
}
.hideBoard{
}
</style>
