<template>
    <div class="hivprevention">
        <section class="hero" id="hivprevention">
            <div class="herotext">
                <h3 class="light">HIV 101</h3>
                <h1>HIV isn't supposed to be scary.</h1>
            </div>
            
            <div class="heroimage">
                <img src="@/assets/hiv-prevention.svg" alt="Gen Z studying beside HIV 101 character">
            </div>
        </section>

        <section class="hiv-stages" id="hiv-risks">
            <div class="stages-title">
                <div class="col-title">
                    <h1>Anyone is at risk <br>for HIV</h1>
                </div>
                <div class="col-desc">
                    <p>
                        To become infected with HIV, infected blood, semen, or vaginal secretions must enter your body.                
                    </p>
                </div>
            </div>
        </section>

        <!-- RISKS -->
        <section class="risks">
            <h3>How You Can Get HIV</h3>
        </section>

            <b-container>
                <b-row class="px-3 px-xl-5">
                    <b-col class="symptoms px-1 pb-5" cols="4" lg="3" v-for="risk in risks" :key="risk.id" v-bind:risk="risks">
                        <div class="symptoms-img">
                            <img :src="require(`@/assets/risk-${risk.image}`)">
                        </div>

                        <h6>{{risk.title}}</h6>
                    </b-col>
                </b-row>
            </b-container>
        
        <!-- NOT RISKS -->
        <section class="risks">
            <h3>How You <strong>Can't</strong> Get HIV</h3>
        </section>

            <b-container>
                <b-row class="px-3 px-xl-5 mt-xl-5">
                    <b-col class="symptoms px-1 px-lg-0 pb-5" cols="4" lg="3" v-for="notrisk in notrisks" :key="notrisk.id" v-bind:notrisk="risks">
                        <div class="symptoms-img">
                            <img :src="require(`@/assets/risk-${notrisk.image}`)">
                        </div>

                        <h6>{{notrisk.title}}</h6>
                    </b-col>
                </b-row>
            </b-container>
        
        <!-- PREVENT -->
        <prevention class="prevent-padding" v-bind:preventions="preventions"/>
        <gettested />

        <!-- LEARN MORE -->
        <b-container class="learn-more">
            <b-row class="px-5 justify-content-center">
                
                <b-col cols="12" class="learn-button my-3" id="learn-text">
                <h1>Learn More</h1>
                </b-col>
                
                <router-link to="/hiv-101" tag="li">
                <b-col cols="12" class="learn-button my-3" id="learn-101">
                <h5>HIV 101</h5>
                <img src="@/assets/hero-hiv101.svg" alt="HIV prevention"> 
                </b-col>
                </router-link>

                <router-link to="/hiv-myths-and-facts" tag="li">
                <b-col cols="12" class="learn-button my-3" id="learn-myths">
                <h5>Myths</h5>
                <img src="@/assets/hiv-myth.svg" alt="HIV myths">
                </b-col>
                </router-link>

                <router-link to="/hiv-living" tag="li">
                <b-col cols="12" class="learn-button my-3" id="learn-living">
                <h5>Living with HIV</h5>
                    <img src="@/assets/hiv-living.svg" alt="Living with HIV"> 
                </b-col>
                </router-link>
            </b-row>
        </b-container>

    <Footer />
    </div>
</template>

<script>
import prevention from "@/components/HIVPrevention";
import gettested from "@/components/GetTested";
import Footer from "@/components/Footer";

    export default {
        name: "hivprevention",
        components: {
            prevention,
            gettested,
            Footer
        },
        data() {
            return {
                risks: [
                    {
                        id: 1,
                        image: "nocondoms.svg",
                        title: "Sex without condoms"
                    },
                    {
                        id: 2,
                        image: "needles.svg",
                        title: "Sharing needles"
                    },
                    {
                        id: 3,
                        image: "pregnancy.svg",
                        title: "Pregnancy"
                    },
                    {
                        id: 4,
                        image: "breastfeeding.svg",
                        title: "Breast-feeding"
                    }
                ],

                notrisks: [
                    {
                        id: 1,
                        image: "nocondoms.svg",
                        title: "Hugging"
                    },
                    {
                        id: 2,
                        image: "sharingwater.svg",
                        title: "Sharing water or food"
                    },
                    {
                        id: 3,
                        image: "air.svg",
                        title: "air"
                    },
                    {
                        id: 4,
                        image: "kissing.svg",
                        title: "kissing"
                    },
                    {
                        id: 5,
                        image: "touch.svg",
                        title: "Touching someone"
                    },
                    {
                        id: 6,
                        image: "toilet.svg",
                        title: "Toilet seats"
                    },
                    {
                        id: 7,
                        image: "air.svg",
                        title: "Insect bites"
                    },
                    {
                        id: 8,
                        image: "sneezes.svg",
                        title: "Sneezes and coughs"
                    },
                    {
                        id: 7,
                        image: "bath.svg",
                        title: "Bathing"
                    },
                    {
                        id: 8,
                        image: "sweat.svg",
                        title: "Sweat"
                    }
                ],

                preventions: [
                    {
                        id: 1,
                        image: "PREP.svg",
                        title: "Take PrEP"
                    },
                    {
                        id: 2,
                        image: "condom.svg",
                        title: "Use condoms"
                    },
                    {
                        id: 3,
                        image: "test.svg",
                        title: "Get tested and treated for STDs"
                    },
                    {
                        id: 4,
                        image: "status.svg",
                        title: "Know partner's HIV status"
                    },
                    {
                        id: 5,
                        image: "needles.svg",
                        title: "Use clean needles when taking drugs"
                    },
                    {
                        id: 6,
                        image: "treatment.svg",
                        title: "Get treatment when HIV+"
                    },

                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
.risks {
    padding: 35px;

    h3 {
        font-size: 18px;
        text-transform: uppercase;
        color: $red;
        text-align: left;
        letter-spacing: 1px;
    }
}

@media screen and (min-width: 768px) {
    .risks {
        padding: 35px 70px;
    }
}

@media screen and (min-width: 1024px) {
    #hiv-risks {
        .stages-title {
            padding: 100px 70px;
            align-items: center;

            .col-title {
                width: 70%;
                padding-right: 20px;
            }
        }
    }

    .prevent-padding {
        margin-top: 100px;
    }
}

@media screen and (min-width: 1280px) {
    #hiv-risks {
        .stages-title {
            padding: 100px 150px;
        }
    }

    .risks {
        padding: 50px 150px;
    }
}
</style>