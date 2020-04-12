<template>
    <div class="myths">
        <section class="hero" id="hivmyths">
            <div class="herotext">
                <h3 class="light">HIV Myths</h3>
                <h1>HIV is not what you think it is.</h1>
            </div>
            
            <div class="heroimage">
                <img src="@/assets/hiv-myth.svg" alt="Characters smiling">
            </div>
        </section>

        <b-container>
            <b-row class="px-5">
                <b-col class="mythsbuttons px-3 py-3 my-3" cols="12" v-for="myth in myths" :key="myth.id" v-bind:myth="myths">
                    <div v-if="myth.image">
                        <img :src="require(`@/assets/${myth.image}`)">
                    </div>
                    
                    <div v-else v-b-modal.modal-facts>
                        <h1>{{ myth.myth }}</h1>
                        <img src="@/assets/icon-circle.svg" class="icon"> 
                    </div>
                </b-col>
            </b-row>
        </b-container>

        <!-- MODAL -->
        <b-modal
            id="modal-facts"
            centered
            title="Modal for Demo Reel"
            size="lg"
            hide-footer
            scrollable: true
            modal-class="modal-container"
            content-class="modal-content"
            header-class="modal-header"
            body-class="modal-body"
            v-for="myth in myths" :key="myth.id" v-bind:myth="myths"
            >
                <div class="videoCont">
                    <youtube
                        :video-id="myth.videoID"
                        ref="youtube"
                        @playing="playing"
                    ></youtube>
                </div>

                <div class="mythsfactsContainer">
                    <div class="mythContent">
                        <h3>Myths</h3>
                        <h2>{{ myth.myth }}</h2>
                    </div>

                    <div class="factsContent">
                        <h3>Facts</h3>
                        <h2>{{ myth.fact }}</h2>
                        <p>
                            {{ myth.description }}
                        </p>

                        <h3>Learn More</h3>
                        <!-- MAKE LINKS DYNAMIC -->
                        <router-link to="#">
                            {{ myth.linkname1 }}
                            <img src="@/assets/icon-forward.svg" alt="Arrow pointing right"> 
                            
                        </router-link><br>
                        <a href="#">
                            {{ myth.linkname2 }}
                            <img src="@/assets/icon-forward.svg" alt="Arrow pointing right"> 
                        </a>

                    </div>
                </div>
        </b-modal>

        <!-- END -->
        <gettested />

        <!-- LEARN MORE -->
        <b-container class="learn-more">
        <b-row class="px-5 justify-content-center">
            <b-col cols="10" class="learn-button my-3" id="learn-text">
            <h1>Learn More</h1>
            </b-col>

            <b-col cols="10" class="learn-button my-3" id="learn-101">
                <h5>HIV 101</h5>
                <img src="@/assets/hero-hiv101.svg" alt="HIV 101">
            </b-col>
            
            <b-col cols="10" class="learn-button my-3" id="learn-prevent">
                <h5>Prevention</h5>
                <img src="@/assets/hiv-prevention.svg" alt="HIV prevention"> 
            </b-col>

            <b-col cols="10" class="learn-button my-3" id="learn-living">
                <h5>Living with HIV</h5>
                <img src="@/assets/hiv-living.svg" alt="Living with HIV"> 
            </b-col>
        </b-row>
        </b-container>
    </div>
</template>

<script>
import gettested from "@/components/GetTested";

    export default {
        name: "myths",
        components: { gettested },
        data() {
            return {
                myths: [
                    {
                        id: 1,
                        myth: "I can get HIV from hugging someone who has HIV.",
                        fact: "You can only get HIV if infected bodily fluids get into your bloodstream through unprotected sex, pregnancy, and sharing needles.",
                        description: "",
                        videoID: "yFcwdeNt32A",
                        linkname1: "HIV Prevention",
                        link1: "/hiv-prevention",
                        link2: "https://hivaidsconnection.ca/get-facts/get-tested",
                        linkname2: "HIV Testing"
                    },
                    {
                        id: 2,
                        myth: "I can treat HIV without any medical help.",
                        fact: "If you are having sex, the only methods of HIV prevention are condoms or pre-exposure prophylaxis (PrEP).",
                        description: "No matter how much you wash your genitals, drink water, or pee, the chances of treating HIV through any kind of method besides medical help is zero. ",
                        videoID: "85SATn36Rks",
                        linkname1: "HIV Prevention",
                        link1: "/hiv-prevention",
                        link2: "https://hivaidsconnection.ca/get-facts/get-tested",
                        linkname2: "HIV Testing"
                    },
                    {
                        id: 3,
                        image: "myth-1.svg"
                    },
                    {
                        id: 4,
                        image: "myth-2.svg",
                    },
                    {
                        id: 5,
                        myth: "If you get HIV, your life is over.",
                        fact: "With treatment, HIV-positive people can live a normal life span and live normal lives.",
                        description: "With treatment, they can be in serious and/or casual relationships and have babies without risking other people.",
                        videoID: "mG75lUmEfb4",
                        linkname1: "Living with HIV",
                        link1: "/hiv-living",
                        linkname2: "Newly Diagnosed?",
                        link2: "https://hivaidsconnection.ca/get-facts/living-hivaidshep-c/hiv"
                    },
                    {
                        id: 6,
                        myth: "If I get infected fluid from an HIV+ person, I will get HIV.",
                        fact: "Undetectable = Untransmittable.",
                        description: "HIV is not always passed on from someone living with HIV, especially if their bodies have undetectable levels of HIV. If you’re scared of the risk, it is important to take an HIV test every time.",
                        videoID: "iPruHLfXP80",
                        linkname1: "HIV Prevention",
                        link1: "/hiv-prevention",
                        link2: "https://hivaidsconnection.ca/get-facts/get-tested",
                        linkname2: "HIV Testing"
                    },
                    {
                        id: 7,
                        myth: "You can only get HIV if you’re gay.",
                        fact: "HIV can be transmitted, no matter what your sexual orientation is.",
                        description: "Like all illnesses, HIV doesn’t choose specific people to affect.",
                        videoID: "mG75lUmEfb4",
                        linkname1: "HIV Prevention",
                        link1: "/hiv-prevention",
                        link2: "https://hivaidsconnection.ca/get-facts/get-tested",
                        linkname2: "HIV Testing"
                    },
                    {
                        id: 8,
                        image: "myth-3.svg"
                    },
                    {
                        id: 9,
                        myth: "Having HIV means that person is dirty or sexually promiscuous.",
                        fact: "The risk of HIV does not increase with the amount of sexual activity.",
                        description: "The risk of HIV increases when one does not practice safe sex, whether it be with one or more partners. (There’s also nothing wrong about being sexually active).",
                        videoID: "cBD6RCwFdoU",
                        linkname1: "HIV Prevention",
                        link1: "/hiv-prevention",
                        link2: "https://hivaidsconnection.ca/get-facts/get-tested",
                        linkname2: "HIV Testing"
                    }
                ]
            }
        }
    }
</script>

<style lang="scss">
// MODAL
.modal-backdrop {
  opacity: 0.9 !important;
  background-color: #ffcc67 !important;
}

.modal-content,
.modal-container,
.modal-header {
  background: none;
}

.modal-body {
    background: white;
    border-radius: 0 0 30px 30px;
    padding: 0 0 30px 0;
}

.modal-content {
  border: none;

  .modal-header {
    border-bottom: none;
    padding: 0 0 10px 0;

    .modal-title {
      display: none;
    }

    .close {
      color: $red;
      opacity: 1;
      transition: transform 0.5s;
    }

    .close:not(:disabled):not(.disabled):focus,
    .close:not(:disabled):not(.disabled):hover {
      opacity: 1;
      transform: rotate(180deg);
    }
  }
}

.mythsfactsContainer {
    display: flex;
    flex-direction: column;
    padding: 0 50px;
    color: $red;

    h3 {
        text-transform: uppercase;
        margin-top: 30px;
    }

    a { color: $red; text-decoration: underline;}

    .factsContent {
        img {
            margin-left: 10px;
        }
    }

    .mythContent,
    .factsContent {
        padding: 0 30px;
    }
}

// VIDEO IN MODAL
.videoCont {
    position: relative;
    width: 100%;

    .video, iframe {
        top: 0 !important;
        left: 0 !important;
        width: 100% !important;
        height: 100% !important;
        margin: 0 auto;
    }
}
</style>

<style lang="scss" scoped>
.mythsbuttons {
    background-color: $red;
    border-radius: 30px;
    width: 204px;
    height: 249px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    color: white;

    img.icon {
        margin-top: 10px;
    }
}

// DIFF COLORS
.mythsbuttons:nth-child(1),
.mythsbuttons:nth-child(9) {
    background-color: $purple;
}

.mythsbuttons:nth-child(2),
.mythsbuttons:nth-child(7) {
    background-color: $yellow;
}

.mythsbuttons:nth-child(3),
.mythsbuttons:nth-child(4),
.mythsbuttons:nth-child(8) {
    background-color: $orange;
}

.mythsbuttons:nth-child(6) {
    background-color: $blue;
}
</style>