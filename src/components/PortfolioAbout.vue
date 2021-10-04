<template>
    <div class="PortfolioAbout">
        <div id="about">
            <h2>Mon portfolio</h2>
            <p>
                Depuis mes début dans le developpement web, j'ai eu l'occasion, durant ma formation
                ou autre, de réaliser divers projet. Ils vont du site vitrine le plus simple aux site
                e-commerce en passant par le réseaux social interne. Je vous laisse les découvrires plus
                en détails.
            </p>
        </div>
    </div>
</template>

<script>
    export default {
        name: "PortfolioAbout"
    }
</script>

<style lang="scss" scoped>
    .PortfolioAbout {
        display: flex;
        justify-content: center;

        #about {
            width: 70vw;

            h2 {
                font-size: 3rem;
                font-weight: 700;
                margin-top: 4vh;
                margin-bottom: 2vh;
                text-align: left;
                text-shadow: -4px 4px 0px #42b983;

                @media screen and (max-width: 475px) {
                    font-size: 2.5rem;
                    text-align: center;
                }
            }

            p {
                text-align: left;
                font-size: 1.25rem;
                padding-bottom: 1vh;
                margin-bottom: 2vh;

                @media screen and (max-width: 475px) {
                    text-align: justify;
                }
            }
        }
    }
</style>