<template> 
<div class="mainTeam">
    <img class="team" :src="require(`../assets/imgs/team.png`)"/>
</div>
</template>

<script>
export default {
    name: 'Team',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.team{
    width: 100%;
    height: auto;
    max-width: 1000px;
}
.mainTeam{
    width: 60%;
    margin: 0 auto;
    resize: both;
}
</style>
