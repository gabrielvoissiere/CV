<template>
  <div id="home">
    <Header />
    <Banner />
    <About />
    <Banner />
    <SkillsSchooling />
    <Softskills />
    <Hobbies />
    <Footer />
  </div>
</template>

<script>
  import Header from '@/components/Header.vue'
  import About from '@/components/About.vue'
  import Banner from '@/components/Banner.vue'
  import SkillsSchooling from '@/components/SkillsSchooling.vue'
  import Softskills from '@/components/Softskills.vue'
  import Hobbies from '@/components/Hobbies.vue'
  import Footer from '@/components/Footer.vue'

  export default {
    name: 'Home',
    data() {
      return {
        //
      }
    },
    components: {
      Header,
      About,
      Banner,
      SkillsSchooling,
      Softskills,
      Hobbies,
      Footer
    },
  }
</script>

<style lang="scss" scoped>
  #home {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
</style>