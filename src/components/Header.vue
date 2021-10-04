<template>
  <header id="header">
    <div id="title">
      <h1>Gabriel Voissiere</h1>
      <h2>Développeur web</h2>
    </div>
    <nav>
      <router-link to="/">CV</router-link>
      <router-link to="/portfolio">Portfolio</router-link>
      <a href="https://github.com/gabrielvoissiere" target="blank">Mon Github</a>
    </nav>
  </header>
</template>

<script>
  export default {
    name: 'Header',
    data() {
      return {
        darkmodeState: "false"
      }
    }
  }
</script>

<style scoped lang="scss">
  header {
    width: 100vw;
    height: auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-bottom: 2vh;
    padding-top: 2vh;
    background-color: white;

    @media screen and (max-width: 475px) {
      flex-direction: column;
    }

    #title {
      margin-left: 15vh;
      text-align: left;

      @media screen and (max-width: 475px) {
        margin-left: 0;
      }

      h1 {
        font-size: 5vh;
        font-weight: 500;

        @media screen and (max-width: 475px) {
          text-align: center;
        }
      }

      h2 {
        font-size: 6vh;
        font-weight: 600;
        text-shadow: -3px 3px 0px #42b983;

        @media screen and (max-width: 475px) {
          font-size: 5vh;
          text-align: center;
        }
      }
    }

    nav {
      width: 30vw;
      height: auto;
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-right: 15vh;

      @media screen and (max-width: 475px) {
        width: 90%;
        margin-right: 0;
        margin-top: 2vh;
      }

      a {
        color: #42b983;
        font-weight: 600;
        text-decoration: none;
        transition: 200ms ease-in-out;
        font-size: 2.5vh;

        &:hover {
          color: black;
        }
      }
    }
  }
</style>