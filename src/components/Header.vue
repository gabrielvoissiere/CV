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

    #title {
      margin-left: 15vh;
      text-align: left;

      h1 {
        font-size: 2rem;
        font-weight: 500;
      }

      h2 {
        font-size: 3.75rem;
        font-weight: 600;
        text-shadow: -3px 3px 0px #42b983;
      }
    }

    nav {
      width: 18%;
      height: auto;
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-right: 15vh;

      a {
        color: #42b983;
        font-weight: 600;
        text-decoration: none;
        transition: 200ms ease-in-out;
        font-size: 1.25rem;

        &:hover {
          color: black;
        }
      }
    }
  }
</style>