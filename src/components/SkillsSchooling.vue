<template>
    <div id="skills">
        <div id="cursus">
            <h2>FORMATION</h2>
            <div class="cursus-block" v-for="item in cursusText" :key="item">
                <p>{{ item.year }}</p>
                <h3>{{ item.title }}</h3>
                <p>{{ item.subtitle}}</p>
                <ul>
                    <li v-for="task in item.task " :key="task">{{ task }}</li>
                </ul>
            </div>
        </div>

        <div id="grid">
            <h2>COMPETENCES</h2>
            <div class="block">
                <h3>Langages web et framework</h3>
                <div class="item" v-for="item in language" :key="item">
                    <div class="ver-line"></div>
                    <div class="hor-line"></div>
                    <p>{{ item }}</p>
                </div>
            </div>
            <div class="block">
                <h3>Logiciels technique</h3>
                <div class="item" v-for="item in software" :key="item">
                    <div class="ver-line"></div>
                    <div class="hor-line"></div>
                    <p>{{ item }}</p>
                </div>
            </div>
            <div class="block">
                <h3>Gestion de projet</h3>
                <div class="item" v-for="item in management" :key="item">
                    <div class="ver-line"></div>
                    <div class="hor-line"></div>
                    <p>{{ item }}</p>
                </div>
            </div>
        </div>

    </div>
</template>

<script>
    export default {
        name: 'SkillsSchooling',
        data() {
            return {
                language: ["HTML", "CSS/SCSS", "Javascript", "Vue JS", "Node JS", "SQL"],
                software: ["Visual Studio Code", "Adobe Illustrator", "Adobe XD", "Suite Office", "Github", "Figma"],
                management: ["Teams", "Discord", "Google Meet", "Zoom"],
                cursusText: [{
                        year: "2020",
                        title: "1ere année de Bachelord",
                        subtitle: "Dans le cadre de mon bachelord, je suis amené à réaliser des missions dans les domaines suivants :",
                        task: ["Communication", "Marketing", "Web design", "Développement web"]
                    },
                    {
                        year: "2020",
                        title: "Formation développeur web (openclassroom et autodidact)",
                        subtitle: "Voici quelques projets réalisés durant ma formation :",
                        task: ["integration de maquette", "site e-commerce", "SEO", "Création d'API"]
                    },
                    {
                        year: "2020",
                        title: "Baccalauréat STI2D - EE Lycée St Eloi - Aix en Provence",
                        subtitle: "Voici quelques projets réalisés pour mon Baccalauréat",
                        task: ["Automatisation d'une VMC (Arduino et C++)",
                            "Programme de calcule (python, javascript)"
                        ]
                    }
                ]
            }
        },
    }
</script>

<style lang="scss" scoped>
    h2 {
        font-size: 3rem;
        font-weight: 700;
        margin-top: 4vh;
        margin-bottom: 2vh;
        text-align: left;
        text-shadow: -4px 4px 0px #42b983;

        @media screen and (max-width: 475px) {
            font-size: 4vh;
            text-align: center;
        }

        @media screen and (min-width: 475px) and (max-width: 1039px) {
            font-size: 5vh;
        }
    }

    #skills {
        width: 70vw;
        display: flex;
        justify-content: space-between;

        @media screen and (max-width: 475px) {
            flex-direction: column;
            width: 85vw;
        }
    }

    #cursus {
        width: 45%;

        @media screen and (max-width: 475px) {
            width: 100%;
        }

        .cursus-block {
            display: flex;
            flex-direction: column;
            text-align: left;
            border-bottom: 3px solid #42b983;
            margin-bottom: 2vh;

            p:first-child {
                margin-bottom: 0.5vh;
                font-size: 1.5rem;
            }

            h3 {
                margin-bottom: 0.5vh;
            }

            li {
                font-size: 1.1rem;
            }
        }
    }

    #grid {
        width: 45%;
        text-align: left;
        display: flex;
        flex-direction: column;
        align-items: flex-end;

        @media screen and (max-width: 475px) {
            width: 100%;
        }

        .block {
            margin-bottom: 4vh;
            width: 50%;

        @media screen and (max-width: 475px) {
            width: 100%;
        }

            @media screen and (min-width: 475px) and (max-width: 1039px) {
                width: 50%;
                margin-right: 5vh;
            }

            h3 {
                margin-bottom: 1vh;
            }

            .item {
                display: flex;
                align-items: center;
                height: 3vh;

                .ver-line {
                    width: 3px;
                    height: 100%;
                    background-color: #42b983;
                }

                .hor-line {
                    width: 3vh;
                    height: 3px;
                    background-color: #42b983;
                    margin-right: 1vh;
                }
            }
        }
    }
</style>