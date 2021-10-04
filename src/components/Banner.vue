<template>
    <div id="language">
      <img src="@/assets/fond.webp" alt="image de fond">
      <div id="filter"></div>
    </div>
</template>

<script>
export default {
    name: 'Banner'
}
</script>

<style lang="scss" scoped>
    #language {
        width: 100vw;
        height: 35vh;
        position: relative;

      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: 0px 65%;
      }

      #filter {
        width: 100%;
        height: 100%;
        background-color: #42b9838a;
        position: absolute;
        top: 0;
      }
    }
</style>