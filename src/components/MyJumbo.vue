<template>
  <div id="jumbo">
    <img src="../assets/images/jumbo.jpg" alt="">
  </div>
</template>

<script>
export default {
    name: 'MyJumbo',
}
</script>

<style lang="scss">
    #jumbo {
        height: 300px;
        width: 100%;

        img {
            height: 100%;
            width: 100%;
            object-fit: cover;
            object-position: 0% 30%;
        }
    }
</style>