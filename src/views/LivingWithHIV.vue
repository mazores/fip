 <template>
    <div class="hivliving">
        <section class="hero" id="hivliving">
            <div class="herotext">
                <h3 class="light">Living with HIV</h3>
                <h1>Life isn't over if you have HIV.</h1>
            </div>
            
            <div class="heroimage">
                <img src="@/assets/hiv-living.svg" alt="Gen Z studying beside HIV 101 character">
            </div>
        </section>

        <div class="steps-section">
            <div class="steps-title">
                <h1>What do I do if I have HIV?</h1>
            </div>

            <div class="steps-content-section">
                <div class="steps-content">
                    <div class="steps-content-icon">
                        <img src="@/assets/life-icons-accept.svg" alt="Heart">
                    </div>
        
                    <div class="steps-content-text">
                        <h1>Accept</h1>
                        <p>
                            Receiving a diagnosis of HIV can be a life-changing event. People can feel many emotions—sadness, hopelessness, and anger. However, the first step is to accept your diagnosis and proceed to taking the measures.
                        </p>
                    </div>
                </div>
        
                <div class="steps-content">
                    <div class="steps-content-icon">
                        <img src="@/assets/life-icons-educate.svg" alt="Brain">
                    </div>
        
                    <div class="steps-content-text">
                        <h1>Brain</h1>
                        <p>
                            Receiving a diagnosis of HIV can be a life-changing event. People can feel many emotions—sadness, hopelessness, and anger. However, the first step is to accept your diagnosis and proceed to taking the measures.
                        </p>
                    </div>
                </div>
        
                <div class="steps-content">
                    <div class="steps-content-icon">
                        <img src="@/assets/life-icons-gethelp.svg" alt="Hands shaking">
                    </div>
        
                    <div class="steps-content-text">
                        <h1>Get Help</h1>
                        <p>
                            There are various resources available for people who are diagnosed with HIV, whether it be medical services, social service providers, or even support groups.
                            <br>By reaching out for help, you will be able to access resources in living with HIV.
                        </p>
                    </div>
                </div>    
            </div>
        </div>


        <b-container class="living mt-5 py-md-5 px-md-5">
            <b-row class="justify-content-center px-4">
                <!-- TREATMENT -->
                <b-col class="col-text pr-md-5" id="treatment" cols="12" md="7" lg="6">
                    <h3 class="light">HIV Treatment</h3>
                    <h2>You can still live life</h2>
                    <p>
                        People often think that your life is over when you get HIV. However, if you get HIV and get treated, you are still going to be able to live a healthy life.
                        <br>While a cure for HIV doesn’t exist yet, antiretroviral therapy (ART), is the combination of several drugs that work together by reducing the amount of virus in your blood and body.
                    </p>
                </b-col>

                <b-col class="col-image" id="treatment-image" md="5" lg="6">
                    <img src="@/assets/life-happy.svg" alt="Happy person surrounded by characters">
                </b-col>
            </b-row>
        </b-container>

        <b-container class="living mt-5 pb-md-5 px-md-5" id="dating-content">
            <b-row class="justify-content-center px-4">
                <!-- DATING -->
                <b-col class="col-text pl-md-5" id="dating" cols="12" md="7" lg="6">
                    <h3 class="light">Dating with HIV</h3>
                    <h2>You can still love and have sex.</h2>
                    <p>
                        You might worry that you can never have a relationship, or sex, or that you won’t be loved but it is absolutely possible to have all these things when you have HIV. it is important to remember that there is much more to you than HIV.
                    </p>

                    <h3 class="light"><br>Telling Partners</h3>
                    <p>
                        Remember that it is your choice how much to tell them and when but bear in mind that it is important that they know, especially before having sex.
                        <br>Telling partners that you have HIV is challenging but it allows them to make decisions that can protect their health or provide added people of mind.
                    </p>

                    <h3 class="light"><br>HIV Treatment for Partners</h3>
                    <p>
                        Your partner will be at risk for HIV if the both of you are sexually active. However, there are different medication available for your partner such as the emergency treatment PEP (post-exposure prophylaxis) and PrEP (pre-exposure prophylaxis).
                    </p>
                </b-col>

                <b-col class="col-image" id="dating-image" cols="12" md="5" lg="6">
                    <img src="@/assets/life-love.svg" alt="Happy person surrounded by characters">
                </b-col>
            </b-row>
        </b-container>

        <b-container class="living my-5 pb-md-5 px-md-5">
            <b-row class="justify-content-center justify-content-md-center align-v-md-center px-4">
                <b-col class="col-text" id="pregnancy" cols="12" md="7" lg="6">
                    <h3 class="light">Pregnancy with HIV</h3>
                    <h2>You can still have healthy babies.</h2>
                    <p>
                        You can pass HIV to your baby during pregnancy, while in labor, while giving birth, or by breastfeeding. The good news is that there are many ways to lower the risk of passing HIV to almost zero. This can be done by talking to a doctor who can work with you to prepare for a healthy pregnancy and help in reducing the risk.                
                    </p>
                </b-col>

                <b-col class="col-image" id="pregnant-image" cols="12" md="5" lg="6">
                    <img src="@/assets/life-pregnant.svg" alt="Happy person surrounded by characters">
                </b-col>
            </b-row>
        </b-container>

        <gettested />
        <!-- LEARN MORE -->
        <b-container class="learn-more">
            <b-row class="px-5 px-md-3 py-md-5 justify-content-center">
                <b-col cols="12" md="2" class="learn-button my-3 mr-md-1" id="learn-text">
                <h1>Learn More</h1>
                </b-col>
                
                <b-col cols="12" md="3" class="learn-button my-3 mx-md-2" id="learn-101">
                <h5>Prevention</h5>
                <img src="@/assets/hero-hiv101.svg" alt="HIV prevention"> 
                </b-col>

                <b-col cols="12" md="3" class="learn-button my-3 mx-md-2" id="learn-prevent">
                <h5>HIV Prevention</h5>
                    <img src="@/assets/hiv-prevention.svg" alt="Prevention"> 
                </b-col>

                <b-col cols="12" md="3" class="learn-button my-3 mx-md-2" id="learn-myths">
                <h5>Myths</h5>
                <img src="@/assets/hiv-myth.svg" alt="HIV myths">
                </b-col>

            </b-row>
        </b-container>

        <Footer />
    </div>
 </template>
 
<script>
import gettested from "@/components/GetTested";
import Footer from "@/components/Footer";

    export default {
        name: "livingwithhiv",
        components: {
            gettested,
            Footer
        }
    }
</script>
 
 <style lang="scss" scoped>
 .steps-section {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    color: $red;
    background: $yellow;
    width: 100%;
    padding: 100px 40px 40px 40px;
    position: relative;
    margin-top: -50px;
    z-index: -1;


    .steps-title {
        margin-bottom: 30px;
        h1 {

        }
    }

    .steps-content-section {
        .steps-content {
            display: flex;
            flex-direction: row;
            justify-content: flex-start;
            width: 100%;
            margin-bottom: 50px;

            .steps-content-icon {
                margin-right: 20px;
                img {
                }
            }

            .steps-content-text {
                text-align: left;

                h3 {
                }

                p {
                }
            }
        }
    }
 }

 .living {
    text-align: left;
    color: $orange;

    .col-text {
        order: 2;
    }

    .col-image {
        order: 1;
        text-align: center;
        img {
            width: 250px;
            padding: 30px 0;
        }
    }
 }

 #pregnant-image {
    text-align: center;
    img {
        width: 150px;
    }
 }

@media screen and (min-width: 768px) {
    .steps-section {
        flex-direction: row;
        padding: 130px 80px 50px 80px;
        
        .steps-title {
            width: 40%;
            padding-right: 50px;
        }

        .steps-content-section {
            width: 60%;
            padding-left: 30px;
            border-left: 5px $red solid;
            
        }
    }

    .living {
        .col-text {
            order: 1;
        }

        .col-image {
            width: 100%!important;
            order: 2;
        }
    }

    #dating-content {
        .col-text {
            order: 2!important;
        }

        .col-image {
            order: 1!important;
        }
    }
}

@media screen and (min-width: 1024px) {
    .living {
        padding: 50px 100px;

        .col-image {
            img {
                width: 100%!important;
            }
        }
    }

    #dating-content {
        .col-image {
            padding-right: 10px;
        }
    }

}

@media screen and (min-width: 1280px) {
    .steps-section {
        flex-direction: row;
        padding: 130px 200px 100px 200px;
        
        .steps-title {
            width: 40%;
            padding-right: 50px;
        }

        .steps-content-section {
            width: 50%;
            padding-top: 80px;
            padding-left: 100px;
            border-left: 5px $red solid;
        }
    }

    .living {
        padding: 30px 200px!important;
    }
}
 </style>