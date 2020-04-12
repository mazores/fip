<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" />  -->
    <b-card-group columns class="masonry">
      <b-card title-tag="h1" class="red cardClass padding-lg">
        <b-card-title><h1>Hello, it’s nice to meet you.</h1></b-card-title>
      </b-card>

      <b-card class="blue cardClass padding-m">
        <b-card-img
        img :src="require('@/assets/home-hi.png')"
        img-alt="Meet HIV character saying hi"
        img-top
        >
        </b-card-img>
      </b-card>

      <b-card title-tag="h1" class="yellow cardClass">
        <b-card-title>
          You've probably never heard of me.
        </b-card-title>
      </b-card>

      <b-card class="yellow cardClass">
        <a href="#" class="card-link">Get to Know</a>
      </b-card>

      <b-card class="red cardClass">
        <b-card-img
        img :src="require('@/assets/home-confused.svg')"
        img-alt="Teen confused about HIV"
        img-top
        >
        </b-card-img>
      </b-card>

      <b-card title-tag="h1" class="purple cardClass">
        <b-card-title>Maybe you heard that HIV is scary but there are ways to prevent it.</b-card-title>
      </b-card>

      <b-card class="purple cardClass">
        <a href="#" class="card-link">Prevent HIV</a>
      </b-card>

      <b-card class="red cardClass">
        <b-card-img
        img :src="require('@/assets/home-ghost-off.svg')"
        img-alt="HIV character hiding under a blanket"
        img-top
        >
        </b-card-img>
      </b-card>

      <b-card class="yellow cardClass">
        <b-card-img
        img :src="require('@/assets/home-ghost.svg')"
        img-alt="HIV character takes off the ghost blanket"
        img-top
        >
        </b-card-img>
      </b-card>
      
      <b-card class="blue cardClass padding-none">
        <b-card-img
        img :src="require('@/assets/home-ew.svg')"
        img-alt="HIV blood in front of text that says gross"
        img-top
        >
        </b-card-img>
      </b-card>

      <b-card title-tag="h1" class="purple cardClass padding-lg">
        <b-card-title>
          <h1>What's the tea?</h1>
        </b-card-title>
      </b-card>

      <b-card title-tag="h1" class="orange cardClass">
        <b-card-title>
          Or.. have you heard the nasty things that they say about me?
        </b-card-title>
      </b-card>

      <b-card class="orange cardClass">
        <a href="#" class="card-link">Bust Myths</a>
      </b-card>

      <b-card class="yellow cardClass">
        <b-card-img
        img :src="require('@/assets/home-teens.svg')"
        img-alt="Group of teens affected by HIV"
        img-top
        >
        </b-card-img>
      </b-card>

      <b-card title-tag="h1" class="blue cardClass padding-m">
        <b-card-title>
          Or about the people that I've affected
        </b-card-title>
      </b-card>

      <b-card class="blue cardClass">
        <a href="#" class="card-link">Living with HIV</a>
      </b-card>

      <b-card class="red cardClass padding-m">
        <b-card-img
        img :src="require('@/assets/home-hivaids.svg')"
        img-alt="HIV and AIDS"
        img-top
        >
        </b-card-img>
      </b-card>
    </b-card-group>

    <div class="cta">
      <h1>It's about time we got to know each other.</h1>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  components: {
    // HelloWorld
  }
};
</script>

<style lang="scss">
.cta {
  padding: 0 35px 30px 35px;
  color: $red;
  
  h1 {
    font-size: 30px!important;
    line-height: 30px!important;
    font-weight: 900;
    text-align: center;
  }

}
.masonry {
  padding: 50px 50px 10px 50px;

  .cardClass {
    border: 0 none!important;
    border-radius: 10px!important;
    text-align: center;
    color: white;
    margin-bottom: 30px!important;

    h1 {
      font-size: 35px!important;
      line-height: 40px!important;
    }
    h4 {
      font-weight: 900;
    }

    a {
      color: white;
      text-transform: uppercase;
      font-weight: 600;
      letter-spacing: 1px;
    }
  }

  .red {
    background-color: $red!important;
  }

  .yellow {
    background-color: $yellow!important;
  }

  .purple {
    background-color: $purple!important;
  }

  .orange {
    background-color: $orange!important;
  }

  .blue {
    background-color: $blue!important;
  }
}

.padding-lg {
  padding: 30px 20px;
}

.padding-m {
  padding: 20 10px;
}

.padding-none {
  padding: 0;
}
</style>
