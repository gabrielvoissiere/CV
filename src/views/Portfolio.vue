<template>
    <div class="portfolio">
    <Header />
    <Banner />
    <PortfolioAbout />
    <Projects />
    <Footer />
    </div>
</template>

<script>
  import Header from '@/components/Header.vue'
  import Banner from '@/components/Banner.vue'
  import PortfolioAbout from '@/components/PortfolioAbout.vue' 
  import Projects from '@/components/Projects.vue' 
  import Footer from '@/components/Footer.vue' 

export default {
    name: "Portfolio",
    data() {
        return {
            //
        }
    },
    components: {
      Header,
      Banner,
      PortfolioAbout,
      Projects,
      Footer
    }
}
</script>

<style lang="scss" scoped>
//
</style>