<template>

    <v-layout>
        <v-btn @click="next">Следующий</v-btn>

        <v-flex xs12 sm6 offset-sm3>
            <v-card>
                <v-container grid-list-sm fluid>
                    <v-layout row wrap>


                        <!--////////////////////////-->
                        <v-flex xs4 d-flex>
                            <v-card flat tile class="d-flex">
                                <svg xmlns="http://www.w3.org/2000/svg" width="250" height="250">
                                    <circle
                                            stroke-width="3"
                                            stroke-miterlimit="10"
                                            cx="125"
                                            cy="125"
                                            r="121.837"></circle>
                                    <path d="M33.802 137.612l17.789-1.114c.385 2.89 1.169 5.091 2.353 6.604 1.925 2.45 4.677 3.674 8.254 3.674 2.668 0 4.726-.626 6.17-1.878 1.445-1.252 2.167-2.704 2.167-4.354 0-1.568-.688-2.972-2.063-4.21-1.376-1.238-4.568-2.407-9.575-3.508-8.2-1.843-14.047-4.292-17.541-7.347-3.522-3.054-5.283-6.947-5.283-11.68 0-3.109.901-6.046 2.704-8.812 1.802-2.765 4.512-4.938 8.13-6.521 3.618-1.582 8.578-2.373 14.879-2.373 7.731 0 13.626 1.438 17.685 4.312 4.058 2.875 6.473 7.45 7.243 13.723L69.09 115.16c-.468-2.724-1.452-4.705-2.951-5.943-1.5-1.238-3.57-1.857-6.211-1.857-2.174 0-3.811.461-4.912 1.383s-1.651 2.043-1.651 3.363c0 .964.454 1.831 1.362 2.601.88.798 2.972 1.541 6.273 2.229 8.172 1.761 14.025 3.543 17.561 5.345 3.535 1.802 6.108 4.039 7.718 6.707 1.61 2.67 2.415 5.654 2.415 8.956 0 3.88-1.073 7.457-3.219 10.731s-5.146 5.758-8.997 7.449c-3.853 1.692-8.708 2.539-14.569 2.539-10.291 0-17.417-1.981-21.379-5.943s-6.205-8.998-6.728-15.108zM92.161 97.125h19.544l13.619 43.542 13.443-43.542h18.975l-22.465 60.505h-20.266l-22.85-60.505zM191.38 135.714v-12.588h28.891v25.796c-5.53 3.77-10.421 6.335-14.672 7.697-4.252 1.361-9.294 2.043-15.127 2.043-7.181 0-13.035-1.225-17.562-3.674-4.526-2.448-8.034-6.094-10.524-10.937s-3.734-10.401-3.734-16.675c0-6.604 1.361-12.347 4.086-17.231 2.724-4.883 6.713-8.591 11.969-11.123 4.1-1.954 9.616-2.93 16.55-2.93 6.687 0 11.687.605 15.003 1.816 3.315 1.211 6.066 3.089 8.254 5.633 2.188 2.545 3.831 5.772 4.933 9.679l-18.036 3.219c-.743-2.284-2.002-4.031-3.776-5.242-1.774-1.21-4.038-1.816-6.789-1.816-4.101 0-7.367 1.424-9.803 4.271-2.435 2.848-3.652 7.354-3.652 13.517 0 6.549 1.231 11.226 3.693 14.032 2.463 2.808 5.896 4.21 10.298 4.21 2.091 0 4.086-.302 5.984-.908 1.898-.604 4.072-1.637 6.521-3.096v-5.695H191.38z"></path>
                                </svg>
                            </v-card>
                        </v-flex>
                        <!--////////////////////////-->


                    </v-layout>
                </v-container>
            </v-card>
        </v-flex>
    </v-layout>
</template>

<script>
    export default {
        data() {
            return {
                images: {
                    logo: require('assets/svg/logo.svg')
                },
                gradient: 'to top right, rgba(63,81,181, .7), rgba(25,32,72, .7)'

            }
        },
        methods: {
            next() {
                this.$router.push('/svg/other')
            }
        }


    }
</script>

<style scoped lang="stylus">
    svg circle
        fill none
        stroke-width 5px
        stroke white
        stroke-dasharray 800
        stroke-dashoffset 800
        opacity 0
        animation 4s circle-outline infinite forwards

    svg
        background-color grey

    svg path
        fill none
        stroke white
        stroke-width 3px
        stroke-dasharray 400
        stroke-dashoffset 400
        animation 8s text-outline infinite alternate


    @keyframes circle-outline {
        from {
            opacity 0;
            stroke-dashoffset: 800;
        }
        to {
            opacity: 1;
            stroke-dashoffset: 0;
        }
    }

    @keyframes text-outline {
        from {
            opacity: 0;
            stroke-dashoffset: 400;
        }
        to {
            opacity: 1;
            stroke-dashoffset: 0;
        }
    }
</style>
