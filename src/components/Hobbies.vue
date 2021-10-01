<template>
    <div id="hobbies">
       <h2>MES CENTRES D'INTERETS</h2>
       <div v-for="item in hobbies" :key="item">
           <h3>{{ item.title }} :</h3>
           <p>{{ item.text }}</p>
       </div>
    </div>
</template>

<script>
export default {
    name: "Hobbies",
    data() {
        return {
            hobbies: [
                {
                title: "Sport",
                text: "vélo de route, VTT, natation"
            },{
                title: "Aéronautique",
                text: "avions de chasse/ligne, ULM et autres"
            },{
                title: "Japon",
                text: "mangas, animes, culture japonaise, gastronomie"
            },{
                title: "Informatique",
                text: "développement frontend, backend, quitter VIM..."
            }
            ]
        }
    },
}
</script>

<style lang="scss" scoped>
#hobbies {
    width: 70vw;
    
    h2 {
        font-size: 3rem;
        font-weight: 700;
        margin-top: 4vh;
        margin-bottom: 2vh;
        text-align: left;
        border-bottom: 3px solid #42b983;
        text-shadow: -4px 4px 0px #42b983;
    }

    div {
        display: flex;
        align-items: flex-end;
        margin-bottom: 1vh;

        p {
            margin-left: 1vh;
            font-size: 1.2rem;
        }
    }
}
</style>