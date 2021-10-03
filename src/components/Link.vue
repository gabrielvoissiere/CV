<template>
    <div id="linkbox">
        <div id="link">
            <a id="linkedin" :href="linkedin" target="blank">Linkedin</a>
            <a id="github" :href="github" target="blank">Github</a>
            <a id="malt" :href="malt" target="blank">Malt</a>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Link",
        data() {
            return {
                linkedin: "https://www.linkedin.com/in/gabriel-voissiere-23663b1b8",
                github: "https://github.com/gabrielvoissiere",
                malt: "https://www.malt.fr/profile/gabrielvoissiere"
            }
        },
    }
</script>

<style lang="scss" scoped>
    #linkbox {
        width: 70vw;
        border-top: 3px solid #42b983;
        margin-top: 4vh;

        #link {
            width: 25%;
            display: flex;
            margin-top: 4vh;

            a {
                color: white;
                text-decoration: none;
                transition: 200ms ease-in-out;
                background-color: red;
                padding: 1vh 2vh;
                border-radius: 10px;
                font-weight: 500;

                &#linkedin {
                    background-color: #036EAA;

                &:hover {
                    box-shadow: -2px 2px 0 #034164;
                }
                }

                &#github {
                    background-color: black;

                &:hover {
                    box-shadow: -2px 2px 0 rgb(54, 54, 54);
                }
                }

                &#malt {
                    background-color: #F25753;

                &:hover {
                    box-shadow: -2px 2px 0 #86332e;
                }
                }
            }

            a {
                margin-right: 2vh;
            }
        }
    }
</style>