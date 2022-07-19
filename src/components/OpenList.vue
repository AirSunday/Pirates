<template> 
<div class="lists">
    <div v-if="width > 650">
        <table style="border:none">
            <tr>
                <td class="mytd">
                    <img class="list" @click="changeFirst" :src="require(`../assets/imgs/list/${listFirst}.png`)"/>
                </td>
                <td class="mytd">
                    <img class="list" @click="changeSecond" :src="require(`../assets/imgs/list/${listSecond}.png`)"/>
                </td>
            </tr>
        </table>
    </div>
    <div v-else>
        <img class="list" @click="changeFirst" :src="require(`../assets/imgs/list/${listFirst}.png`)"/>
        <img class="list" @click="changeSecond" :src="require(`../assets/imgs/list/${listSecond}.png`)"/>
    </div>
</div>
</template>

<script>
export default {
    name: 'OpenList',
    data() {
        return {
            listFirst: "listClose",
            listSecond: "listClose",
            width: window.innerWidth,
        };
    },
    methods: {
        updateWidth() {
            this.width = window.innerWidth;
        },
        changeFirst(){
            this.listFirst =this.listFirst == "listClose" ? "listOpen" : "listClose"
        },
        changeSecond(){
            this.listSecond =this.listSecond == "listClose" ? "listOpen" : "listClose"
        },
    },
    created() {
        window.addEventListener("resize", this.updateWidth);
    },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.list{
    width: 100%;
    height: auto;
    max-width: 500px;
}
.mytd{
    vertical-align: top;
}
.lists{
    width: 60%;
    margin: 0 auto;
    resize: both;
}
</style>
