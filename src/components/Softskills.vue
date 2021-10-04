<template>
    <div id="softskills">
       <h2>QUALITES PERSONNELLES</h2>
       <div v-for="item in softskills" :key="item">
           <p>• {{ item }}</p>
       </div>
    </div>
</template>

<script>
export default {
    name: "Softskills",
    data() {
        return {
            softskills: [
                "Curieux","Volontaire","Sérieux","Motivé","Sociable","Investi"
            ]
        }
    },
}
</script>

<style lang="scss" scoped>
#softskills {
    width: 70vw;

        @media screen and (max-width: 475px) {
            width: 85vw;
        }
    
    h2 {
        font-size: 3rem;
        font-weight: 700;
        margin-top: 4vh;
        margin-bottom: 2vh;
        text-align: left;
        border-bottom: 3px solid #42b983;
        text-shadow: -4px 4px 0px #42b983;

        @media screen and (max-width: 475px) {
            font-size: 4vh;
        }
    }

    div {
        display: flex;
        align-items: flex-end;
        margin-bottom: 1vh;

        p {
            font-size: 1.2rem;
        }
    }
}
</style>