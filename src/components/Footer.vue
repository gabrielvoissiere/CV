<template>
    <footer>
        <div id="box">
            <div id="contact">
                <h2>CONTACT</h2>
                <p>{{ email }}</p>
                <p>{{ tel }}</p>
                <div id="link">
                    <a :href="linkedin" target="blank">LinkedIn</a>
                    <a :href="github" target="blank">Github</a>
                    <a :href="malt" target="blank">Malt</a>
                </div>
            </div>
            <p>© Gabriel Voissiere - {{ getYear }}</p>
        </div>
    </footer>
</template>

<script>
    export default {
        name: 'Footer',
        data() {
            return {
                email: "gabvoissiere.pro@yahoo.com",
                tel: "06 95 90 13 10",
                linkedin: "https://www.linkedin.com/in/gabriel-voissiere-23663b1b8",
                github: "https://github.com/gabrielvoissiere",
                malt: "https://www.malt.fr/profile/gabrielvoissiere"
            }
        },
        computed: {
            getYear() {
                let getdate = new Date()
                let year = getdate.getFullYear()
                return year
            }
        }
    }
</script>

<style scoped lang="scss">
    footer {
        width: 100vw;
        height: auto;
        display: flex;
        align-items: center;
        justify-content: center;
        background-color: #42b983;
        color: white;
        margin-top: 4vh;

        p {
            font-size: 1.5rem;
        }

        #box {
            width: 70vw;
            display: flex;
            align-items: center;
            justify-content: space-between;

            #contact {
                height: 100%;
                display: flex;
                flex-direction: column;
                text-align: left;
                padding-bottom: 5vh;

                h2 {
                    font-size: 3rem;
                    font-weight: 700;
                    margin-top: 5vh;
                    margin-bottom: 1vh;
                    text-align: left;
                    text-shadow: -4px 4px 0px black;
                }

                p,
                a {
                    font-size: 1.2rem;
                    margin: 2px 0;
                }

                #link {
                    width: 100%;
                    display: flex;

                    a {
                        color: white;
                        text-decoration: none;
                        border-bottom: 2px solid white;
                        transition: 200ms ease-in-out;

                        &:hover {
                            color: black;
                            border-bottom: 2px solid black;
                        }
                    }

                    a {
                        margin-right: 2vh;
                    }
                }
            }
        }
    }
</style>