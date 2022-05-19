<template>
    <div class="playlist">
        <div class="ms-container pt-4">
            <div class="row row-cols-6 gap-4">
                <AppSongCard class="ms-card" v-for="(item, index) in song" :key="index" :songCard="item" />
            </div>
        </div>
    </div>
</template>

<script>
import AppSongCard from "./AppSongCard.vue";
import axios from "axios";

export default {
    name: 'AppSong',
    components: {
        AppSongCard,
    },
    data() {
        return {
            song: [],
        };
    },
    created() {
        axios
        .get("https://flynn.boolean.careers/exercises/api/array/music")
        .then((resp) => {
            this.song = resp.data.response;
        });
    },
}
</script>

<style scoped lang="scss">
@import "../style/common.scss";
@import "../style/variables.scss";

.playlist {
    background-color: $m-backcolor;
    height: calc(100vh - 60px);

    .ms-container {
        width: 60%;
        margin: 0 auto;
    }
}

</style>