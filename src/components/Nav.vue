<template>
    <div>
        <!-- MOBILE -->
        <div class="mobile-nav">
            <div class="logo">
                <img src="@/assets/logo.svg" alt="HIV prevention"> 
            </div>

            <div v-show="!isLearnMoreActive" class="burger-menu">
                <img @click="toggleMenu()" src="@/assets/icon-menu.svg" alt="Burger menu"> 
            </div>
        </div>

        <div class="mobile-nav-open" id="get-to-know" v-bind:class="{ open: isLearnMoreActive }">
            <ul>
                <li @click="toggleLearnMore(); toggleArrowRotate()"><a href="#">
                    <img src="@/assets/icon-forward.svg" alt="Arrow pointing right" class="back" v-bind:class="{ rotate: isArrowRotated }"> Get to Know 
                </a></li>
            </ul>

            <div class="learn-more-menu">
                <div class="learn-button" id="learn-101" @click="toggleLearnMore(); toggleMenu()">
                    <router-link to="/hiv-101" tag="li">
                    <h5>HIV 101</h5>
                    <img src="@/assets/hero-hiv101.svg" alt="HIV 101"> 
                    </router-link>
                </div>

                <div class="learn-button" id="learn-prevent" @click="toggleMenu(); toggleLearnMore(); toggleArrow(); toggleArrowRotate()">
                    <router-link to="/hiv-prevent" tag="li">
                    <h5>Prevention</h5>
                    <img src="@/assets/hiv-prevention.svg" alt="HIV prevention"> 
                    </router-link>
                </div>

                <div class="learn-button" id="learn-myths" @click="toggleMenu(); toggleLearnMore(); toggleArrow(); toggleArrowRotate()">
                    <router-link to="hiv-myths-and-facts" tag="li">
                    <h5>Myths</h5>
                    <img src="@/assets/hiv-myth.svg" alt="HIV myths">
                    </router-link>
                </div>

                <div class="learn-button" id="learn-living" @click="toggleMenu(); toggleLearnMore(); toggleArrow(); toggleArrowRotate()">
                    <router-link to="hiv-living" tag="li">
                    <h5>Living with HIV</h5>
                    <img src="@/assets/hiv-living.svg" alt="Living with HIV"> 
                    </router-link>
                </div>
            </div>
        </div>

        <div class="mobile-nav-open" v-bind:class="{ open: isActive }">
            <ul>
                <li><a href="#">Home</a></li>
                <li @click="toggleLearnMore(); toggleArrow(); toggleArrowRotate()"><a href="#">
                    Get to Know <img v-bind:class="{ rotate: isSecondArrow }" src="@/assets/icon-forward.svg" alt="Arrow pointing right"> 
                </a></li>
                <li><a href="https://hivaidsconnection.ca/" target="_blank">RHAC</a></li>
            </ul>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Nav",
        data() {
            return {
                isActive: false,
                isLearnMoreActive: false,
                isArrowRotated: false,
                isSecondArrow: false
            };
        },
        methods: {
            toggleMenu: function() {
                this.isActive = !this.isActive
            },

            toggleLearnMore: function() {
                this.isLearnMoreActive = !this.isLearnMoreActive
            },

            toggleArrow: function() {
                this.isSecondArrow = !this.isSecondArrow
            },

            toggleArrowRotate: function() {
                this.isArrowRotated = !this.isArrowRotated
            }


        }
    }
</script>

<style lang="scss" scoped>
.open {
    right: 0vw !important;
}

.rotate {
    transform: rotate(-180deg);
}

.mobile-nav {
    background-color: white;
    width: 100vw;
    z-index: 300;
    position: fixed;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    padding: 30px 20px;
    -webkit-box-shadow: 0px 4px 33px -15px rgba(0,0,0,0.36);
    -moz-box-shadow: 0px 4px 33px -15px rgba(0,0,0,0.36);
    box-shadow: 0px 4px 33px -15px rgba(0,0,0,0.36);

    .logo {
        img {
            width: 80%;
        }
    }

    .burger-menu {

    }
}

#get-to-know {
    z-index: 2;
    right: -100vw;
    transition: right 1s ease-in-out 0.1s;

    img.back {
        transform: rotate(-180deg);
        margin-right: 10px;
        transition: transform 1s ease-in-out 0.1s;
    }

    .learn-more-menu {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        align-items: center;
        justify-content: space-around;
        margin-top: 15px;

        .learn-button {
            width: 45%;
            height: 133px;
            text-align: center;
            color: white;
            border-radius: 10px;
            padding: 25px 25px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: space-evenly;
            margin-bottom: 15px;

            li {
                list-style-type: none;
            }

            h5 {
                font-weight: 900;
                font-size: 12px;
                text-transform: uppercase;
            }
            
            img {
                height: 75px;
                margin-top: 10px;
            }
        }
    }
}

.mobile-nav-open {
    height: 100vh;
    width: 100vw;
    right: -100vw;
    top: 80px;
    background-color: #FCFCFC;
    display: flex;
    flex-direction: column;
    align-items: flex-end;
    text-align: right;
    padding: 0 30px;
    position: fixed;
    z-index: 1;
    transition: right 1s ease-in-out 0.1s;

    ul {
        padding-top: 30px;
        li {
            padding: 15px 0;
            a {
                color: $red;
                text-transform: uppercase;
                letter-spacing: 1px;

                img {
                    margin-left: 10px;
                    transition: transform 1s, opacity 1s ease;
                }
            }
        }
    }
}
</style>