<template>
    <div class="hiv-stages">
        <div class="stages-title">
            <div class="col-title">
                <h3>Stage Three -</h3>
                <h1>Symptomatic HIV</h1>
            </div>
            <div class="col-desc">
                <p>
                    By this stage, a person’s immune system is severely damaged. They will. Be more likely to get serious infections or diseases that the body would otherwise be able to fight off.
                </p>
            </div>
        </div>

        <b-container>
            <b-row class="px-3">
                <b-col class="symptoms px-1 pb-5" cols="4" v-for="threesymptom in threesymptoms" :key="threesymptom.id" v-bind:threesymptom="threesymptoms">
                    <div class="symptoms-img">
                        <img :src="require(`@/assets/symptoms-${threesymptom.image}`)">
                    </div>

                    <h6>{{threesymptom.title}}</h6>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
    export default {
        name: "stagethree",
        props: ["threesymptoms"]
    }
</script>

<style lang="scss" scoped>

</style>