<template>
    <div class="PortfolioAbout">
        <div id="projects">
            <div class="project" v-for="item in projects" :key="item">
                <h3>{{ item.title }}</h3>
                <img :src="require(`@/assets/${item.image}`)" :alt="item.title">
                <p>{{ item.sumup }}</p>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Projects",
        data() {
            return {
                projects: [
                    {
                    title: "Frontend d'un site e-commerce",
                    image: "orinoco.svg",
                    sumup: "Site e-commerce réaliser durant mes études, en HTML, SCSS, et JS. Les informations venant d'une API"
                },
                {
                    title: "Intégration d'une maquette",
                    image: "reservia.svg",
                    sumup: "Integration d'une maquette de site sur Adobe XD en HTML et CSS durant mes études"
                },
                {
                    title: "Site d'architecture",
                    image: "ecvarchitecture.svg",
                    sumup: "Création d'un site web sur 3 types d'architecture avec une page par type"
                },
                {
                    title: "SEO et accessibilité d'un site de designer",
                    image: "lachouetteagence.svg",
                    sumup: "Durant mes études, mise en place du référencement naturel du site, et mise à niveaux de l'accessibilité"
                },
                {
                    title: "Systeme de messagerie interne",
                    image: "groupomania.svg",
                    sumup: "Création du front et du back d'un systeme de messagerie interne avec envoie de text et images sous forme de forum"
                },
                {
                    title: "Création de mon CV/Portfolio",
                    image: "portfolio.svg",
                    sumup: "Réalisation de mon CV/Portfolio pour vous faire découvrire qui je suis, ce que je fait, et ce que j'ai fait "
                },
                {
                    title: "Création d'une API sécurisée",
                    image: "sopecoko.svg",
                    sumup: "Création d'une API sécurisée avec MongoDB et NodeJS pour un site d'avis gastronomique durant mes études"
                },
                {
                    title: "Ajout d'animation sur un site",
                    image: "ohmyfood.svg",
                    sumup: "Ajout d'animation en SCSS pour dynamiser un site réaliser precedament"
                }
                ]
            }
        },
    }
</script>

<style lang="scss" scoped>
    .PortfolioAbout {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;

        #projects {
            width: 70vw;
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2vh;
            margin: 2vh 0;

            .project {
                display: flex;
                flex-direction: column;
                justify-content: flex-start;
                align-items: center;
                padding: 2vh 0;

                img {
                    width: 100%;
                    height: 80%;
                    object-fit: cover;
                    margin-top: 1vh;
                    transition: 200ms ease-in-out;

                &:hover {
                    box-shadow: -8px 8px 0px #42b983;
                    cursor: pointer;
                }
                }

                p {
                    margin-top: 1vh;
                }
            }
        }
    }
</style>