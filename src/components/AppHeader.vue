<template>
    <div class="col-12 ms-header d-flex align-items-center">
        <img class="ms-4" src="../assets/logo-small.svg" alt="">
    </div>
</template>

<script>
export default {
  name: 'AppHeader',

}
</script>

<style scoped lang="scss">
@import "../style/common.scss";
@import "../style/variables.scss";


.ms-header {
    height: 60px;
    background-color: $h-backcolor;

    img {
        height: 70%;
    }
}

</style>