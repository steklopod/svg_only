<template>

    <v-img
            :gradient="gradient"
            :src="images.sample"
            style="max-height: 20vh"
    >

    </v-img>


</template>

<script>
    export default {
        data() {
            return {
                images: {
                    sample: require('assets/svg/logo.svg')
                },
                gradient: 'to top right, rgba(63,81,181, .7), rgba(25,32,72, .7)',
                errored: false
            }
        }

    }
</script>

<style scoped lang="stylus">
    h3
        font-family 'Pacifico', 'Montserrat Alternates' !important

</style>
