<template>  
<div>
    <table>
        <td>
            <img class="wanted" src="../assets/imgs/wanted.png"/>
        </td>
        <td>
            <img class="gunWithPapaer" src="../assets/imgs/gunWithPapaer.png"/>
            <!-- <p class="textInPapaer">
                                Pirate's Island is a collection of hand-drawn 5555
                                unique Pirates. Holding a Pirate allows you to participate
                                in coordinating the Pirate Treasury. The Pirate Treasury will 
                                receive 50% from mint and 5% OpenSea royalties. This amount 
                                will be raffled off in the treasure hunt.</p> -->
        </td>
    </table>
</div>
</template>

<script>
export default {
    name: 'FirstInfo',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.wanted{
    width: 70%;
    height: auto;
    min-width: 150px;
    float: right;
}
.gunWithPapaer{
    width: 80%;
    height: auto;
    min-width: 250px;
    float: left;
}
.textInPapaer{
    position: absolute;
    font-size:calc(2px + 1.5vw);
    margin-top: 5vw;
    margin-left: 5vw;
    margin-right: 25vw;
}
</style>
