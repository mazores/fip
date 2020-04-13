<template>
    <div class="prevention">
        <section class="title">
            <h1>How do you prevent it?</h1>
        </section>

        <b-container>
            <b-row class="px-3 mt-5  px-lg-4 ">
                <b-col class="symptoms px-1 pb-5" cols="6" md="4" v-for="prevention in preventions" :key="prevention.id" v-bind:prevention="preventions">
                    <div class="symptoms-img">
                        <img :src="require(`@/assets/prevent-${prevention.image}`)">
                    </div>

                    <h6>{{prevention.title}}</h6>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
    
    export default {
        name: "prevention",
        props: ["preventions"]

    }
</script>

<style lang="scss" scoped>
.prevention {
    background-color: $yellow;
    padding-top: 50px;

    .title {
        padding: 0 25px;

        h1 {
            color: $red;
            text-align: center;
        }
    }
}

@media screen and (min-width: 768px) {
    .prevention {
        padding-top: 100px;
        padding-bottom: 80px;

        .title {
            h1 {
                font-size: 60px!important;
                padding-bottom: 50px!important;
            }
        }
    }
}

@media screen and (min-width: 1024px) {
    .prevention {
        .symptoms {
            .symptoms-img {
                img {
                    height: 230px;
                }
            }
        }
    }
}
</style>