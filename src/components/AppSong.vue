<template>
    <div class="playlist">
        <div v-if="success" class="ms-container pt-4">
            <div class="row row-cols-1">
                <AppSearch @searchSelected="songSelected($event)" />
            </div>
            <div class="row row-cols-6 gap-4">
                <AppSongCard class="ms-card" v-for="(item, index) in songFiltered" :key="index" :songCard="item" />
            </div>
        </div>
        <div v-else class="container">
            <div class="my-loader text-center"><AppLoading /></div>
        </div>
    </div>
</template>

<script>
import AppSongCard from "./AppSongCard.vue";
import AppLoading from "./AppLoading";
import AppSearch from "./AppSearch.vue";
import axios from "axios";

export default {
    name: 'AppSong',
    components: {
        AppSongCard,
        AppLoading,
        AppSearch,
    },
    data() {
        return {
            song: [],
            success: false,
            genre: "",
        };
    },
    created() {
        axios
        .get("https://flynn.boolean.careers/exercises/api/array/music")
        .then((resp) => {
            this.song = resp.data.response;
            this.success = resp.data.success;
        });
    },

      computed: {
        songFiltered() {
        const filteredArray = this.song.filter((item) => {
        return item.genre.includes(this.genre);
        });
        return filteredArray;
        },
    },
    methods: {
        songSelected(event) {
        this.genre = event;
        },
    },
}
</script>

<style scoped lang="scss">
@import "../style/common.scss";
@import "../style/variables.scss";

.playlist {
    background-color: $m-backcolor;
    height: 100vh;

    .ms-container {
        width: 60%;
        margin: 0 auto;

        .ms-card {
            cursor: pointer;
            transition: 0.3s;
            &:hover {
                opacity: 0.7;
            }
        }
    }

    .my-loader {
        position: absolute;
        top: 50%;
        right: 50%;
        transform: translate(50%, -50%);
    }
}

</style>