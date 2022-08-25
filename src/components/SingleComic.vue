<template>
    <div class="comic-card">
        <img :src="comicThumb" />
        <h6 class="text-white py-1">{{comicSeries}}</h6>
    </div>

</template>

<script>
export default {
    name: 'SingleComic',
    props: {
        comicThumb: String,
        comicSeries: String,
    }
}
</script>

<style lang="scss">
    .comic-card {
        min-height: 250px;
        width: calc(100% / 6 - 20px);
        margin: 10px;
        display: flex;
        flex-direction: column;

        
        

        img {
        height: 170px;
        width: 170px;
        object-fit: cover;
        object-position: 0% 0%;
        
            &:hover {
                cursor: pointer;
            }
        }

        h4 {
            fonts-size: 14px;
        }
    }
</style>