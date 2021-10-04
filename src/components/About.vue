<template>
    <div id="about">
        <img src="@/assets/photo.jpg" alt="photo">
        <p>
            Titulaire d'un Bac STI2D, je suis maintenant <span>étudiant</span> en Bachelord
            Chef de projet <span>digital</span> mais également développeur freelance.
            <br><br>
            J'ai découvert le <span>développement web</span> en seconde, à l'âge de 15 ans,
            j'ai été piqué par la passion de ce métier instantanément. J'ai alors
            commencé à me former sur youtube et internet en <span>autodidacte</span>.
            <br><br>
            Extrêmement <span>motivé</span> afin de développer constamment toutes mes
            compétences et évoluer professionnellement. Je suis confiant dans
            ma capacité à proposer des <span>idées</span> intéressantes pour chacun de mes
            projets. <span>Sociable</span> et aimable, je travaille aussi bien seul qu'en <span>équipe</span>.
            And I also speak English if you want.
            <br><br>
            <strong>
                En résumer, <span>j'ai {{ age }} ans</span>, je possède un Bac STI2D, et
                je suis un passionné du <span>développement web</span> qui en a fait son métier.
            </strong>
        </p>
    </div>
</template>

<script>
    export default {
        name: 'About',
        data() {
            return {
                age: ""
            }
        },
        mounted() {
            let date = new Date()
            this.age = date.getFullYear() - 2001
        },
    }
</script>

<style lang="scss" scoped>
    #about {
        width: 70vw;
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 5vh;
        margin-top: 5vh;

        @media screen and (max-width: 475px) {
            flex-direction: column;
        }

        @media screen and (min-width: 475px) and (max-width: 1030px) {
            width: 85vw;
        }

        img {
            width: 35%;
            height: 50vh;
            object-fit: cover;
            box-shadow: -4px 4px 0px #42b983;

            @media screen and (max-width: 475px) {
                width: 100%;
                height: 40vh;
            }
        }

        p {
            width: 55%;
            text-align: left;
            font-size: 1.25rem;
            padding-bottom: 4vh;
            border-bottom: 3px solid #42b983;

            @media screen and (max-width: 475px) {
                width: 100%;
                margin-top: 2vh;
                text-align: justify;
            }

            @media screen and (min-width: 475px) and (max-width: 1030px) {
                display: 70%;
            }

            span {
                color: #42b983;
            }
        }
    }
</style>