<template>
    <div class="song-card">
        <img class="pt-2" :src="songCard.poster" alt="">
        <h5 class="text-center pt-3"> {{songCard.title}} </h5>
        <span class="d-block text-center"> {{songCard.author}} </span>
        <span class="d-block text-center"> {{songCard.year}} </span>
    </div>
</template>

<script>
export default {
  name: 'AppSongCard',
    props: {
        songCard: Object,
    }
}
</script>

<style scoped lang="scss">
@import "../style/common.scss";
@import "../style/variables.scss";

.song-card {

    background-color: $card-color;
    width: calc(100% / 5);

    img {
        width: 100%;
    }

    h5 {
        color: $white;
        text-transform: uppercase;
        font-weight: bold;
    }

    span {
        color: $t-grey;
        text-transform: uppercase;
    }
}


</style>