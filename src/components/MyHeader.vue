<template>
    <header>
        <img src="../assets/img/spotify-logo.png" alt="logo spotify">
    </header>
</template>

<script>

export default {
    name: 'MyHeader',

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    header {
        height: 100px;
        background-color: #2e3a46;
        display: flex;
        justify-content: flex-start;
        align-items: center;

        img {
            width: auto;
            height: 80px;
            padding-left: 30px;
        }
    }
</style>
