<template>
  <div class="hiv101">
    <section class="hero" id="hiv101">
      <div class="herotext">
        <h3 class="light">HIV 101</h3>
        <h1>Let's get to know each other!</h1>
      </div>
      
      <div class="heroimage">
        <img src="@/assets/hero-hiv101.svg" alt="Gen Z studying beside HIV 101 character">
      </div>
    </section>

    <section class="hiv-info" id="hiv">
        <div class="col-text">
            <h1>The Human Immunodeficiency Virus (HIV)</h1>
            <p>HIV is a virus that attacks the immune system, which is the body’s natural defense system. This means HIV interferes with your body’s ability to fight infection and disease.</p>
        </div>

        <div class="col-img">
            <img src="@/assets/hiv101-hiv.svg" alt="HIV character">
        </div>
    </section>

    <section class="hiv-info" id="aids">
        <div class="col-img">
            <img src="@/assets/hiv101-aids.svg" alt="AIDS character">
        </div>
        <div class="col-text">
            <h2>When left untreated,</h2>
            <h1>HIV leads <br>to AIDS</h1>
            <p>AIDS stands for Acquired Immunodeficiency Syndrome. Having HIV does not mean you have AIDS but when HIV is left untreated and completely breaks down your immune system over several years, it leads to AIDS.</p>
        </div>
    </section>

    <!-- STAGES -->
    <stageone v-bind:onesymptoms="onesymptoms" />
    <stagetwo />
    <stagethree v-bind:threesymptoms="threesymptoms" />

    <!-- END PAGE -->
    <gettested />

    <!-- LEARN MORE -->
    <b-container class="learn-more">
      <b-row class="px-5 px-md-3 py-md-5 justify-content-center">
        <b-col cols="12" md="2" class="learn-button my-3 mr-md-1" id="learn-text">
          <h1>Learn More</h1>
        </b-col>
        
        <b-col cols="12" md="3" class="learn-button my-3 mx-md-2" id="learn-prevent">
          <h5>Prevention</h5>
          <img src="@/assets/hiv-prevention.svg" alt="HIV prevention"> 
        </b-col>

        <b-col cols="12" md="3" class="learn-button my-3 mx-md-2" id="learn-myths">
          <h5>Myths</h5>
          <img src="@/assets/hiv-myth.svg" alt="HIV myths">
        </b-col>

        <b-col cols="12" md="3" class="learn-button my-3 mx-md-2" id="learn-living">
          <h5>Living with HIV</h5>
            <img src="@/assets/hiv-living.svg" alt="Living with HIV"> 
        </b-col>
      </b-row>
    </b-container>

    <Footer />
  </div>
</template>

<script>
import stageone from "@/components/HIV101StageOne";
import stagetwo from "@/components/HIV101StageTwo";
import stagethree from "@/components/HIV101StageThree";
import gettested from "@/components/GetTested";
import Footer from "@/components/Footer";

  export default {
    name: "HIV101",
    components: {
      stageone,
      stagetwo,
      stagethree,
      gettested,
      Footer
    },
    data() {
      return {
        onesymptoms: [
          {
            id: 1,
            image: "fever.svg",
            title: "Fever"
          },
          {
            id: 2,
            image: "bodyrash.svg",
            title: "Body rash"
          },
          {
            id: 3,
            image: "sorethroat.svg",
            title: "Sore throat"
          },
          {
            id: 4,
            image: "lymphglands.svg",
            title: "Swollen lymph glands"
          },
          {
            id: 5,
            image: "headache.svg",
            title: "Headache"
          },
          {
            id: 6,
            image: "diarrhea.svg",
            title: "Diarrhea"
          },
          {
            id: 7,
            image: "jointaches.svg",
            title: "Joint aches and pains"
          },
          {
            id: 8,
            image: "musclepain.svg",
            title: "Muscle pain"
          },
          {
            id: 9,
            image: "cough.svg",
            title: "Coughs"
          },
          {
            id: 10,
            image: "nightsweats.svg",
            title: "Night sweats"
          }
        ],

        threesymptoms: [
          {
            id: 1,
            image: "fever.svg",
            title: "Fever"
          },
          {
            id: 2,
            image: "fatigue.svg",
            title: "Fatigue"
          },
          {
            id: 3,
            image: "lymphglands.svg",
            title: "Swollen lymph glands"
          },
          {
            id: 4,
            image: "diarrhea.svg",
            title: "Diarrhea"
          },
          {
            id: 5,
            image: "weightloss.svg",
            title: "Weight loss"
          },
          {
            id: 6,
            image: "oralyeast.svg",
            title: "Oral yeast infection"
          },
          {
            id: 7,
            image: "shingles.svg",
            title: "Shingles"
          },
          {
            id: 8,
            image: "pneumonia.svg",
            title: "Pneumonia"
          },
          {
            id: 9,
            image: "nightsweats.svg",
            title: "Night sweats"
          },
          {
            id: 10,
            image: "mouthskinprobs.svg",
            title: "Mouth/skin problems"
          }
        ]
      }
    }
  }
</script>

<style lang="scss" scoped>

#hiv {
  background-color: #44C3E8;
  z-index: -5;
}

#aids {
  background-color: $purple;
  z-index: -6;

  p {
    color: white!important;
  }
}

.hiv-info {
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  padding: 35px 10%;
  border-radius: 0 0 50px 50px;
  margin-top: -50px;
  padding-top: 100px;
  padding-bottom: 50px;
  position: relative;

  .col-text {
    order: 2;
    text-align: left;
    margin-top: 25px;

    h1, h2 {
      color: white;
      line-height: 35px;
    }

    p {
      color: black;
      margin-top: 10px;
    }
  }

  .col-img {
    order: 1;
    text-align: center;

    img {
      width: 30%;
    }
  }
}

@media screen and (min-width: 768px) {
  .hiv-info {
    padding: 100px 70px;
    flex-direction: row;
    align-items: center;

    .col-text {
      width: 60%;
    }

    .col-img {
      width: 40%;
      text-align: center;

      img {
        width: 60%;
      }
    }
  }

  #hiv {
    .col-text {
      order: 1;
    }

    .col-img {
      order: 2;
    }
  }
}

@media screen and (min-width: 1024px) {
  .hiv-info {
    padding: 150px 150px;
  }
}

@media screen and (min-width: 1280px) {
  .hiv-info {
    padding: 150px 250px;
  }   
}

@media screen and (min-width: 1024px) {
  .hiv-info {
    justify-content: space-between;
    .col-text {
      width: 50%;
    }
  }

}
</style>