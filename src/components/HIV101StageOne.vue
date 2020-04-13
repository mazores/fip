<template>
    <div class="hiv-stages">
        <div class="stages-title">
            <div class="col-title">
                <h3>Stage One -<br>Primary Infection</h3>
                <h1>Acute HIV</h1>
            </div>
            <div class="col-desc">
                <p>
                    This stage is around one to four weeks after getting HIV. These flu-like symptoms can be so mild that you don’t notice them but the amount of virus in your bloostream is quite high. As a result, the infection spreads more easily.
                </p>
            </div>
        </div>

        <b-container>
            <b-row class="px-3 px-lg-0">
                <b-col class="symptoms px-1 px-lg-0 pb-5" cols="4" lg="3" v-for="symptom in onesymptoms" :key="symptom.id" v-bind:symptom="onesymptoms">
                    <div class="symptoms-img">
                        <img :src="require(`@/assets/symptoms-${symptom.image}`)">
                    </div>

                    <h6>{{symptom.title}}</h6>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>


<script>
    export default {
        name: "stageone",
        props: ["onesymptoms"]
    }
</script>

<style lang="scss" scoped>

</style>