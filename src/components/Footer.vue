<template>
    <div class="footer">
        <img src="@/assets/logo.svg" alt="Meet HIV Logo" class="logo"> 
        <h3>A campaign By Regional HIV/AIDS Connection</h3>
        <ul class="social">
            <li><a href="#"><img src="@/assets/icon-facebook.svg" alt="Facebook icon"></a></li>
            <li><a href="#"><img src="@/assets/icon-instagram.svg" alt="Instagram icon"></a></li>
            <li><a href="https://www.youtube.com/channel/UC1x21wCXJQ0vltkF97xzS2g/" target="_blank"><img src="@/assets/icon-youtube.svg" alt="Youtube icon"></a></li>
    </ul>
    </div>
</template>

<script>
    export default {
        name: "Footer"
    }
</script>

<style lang="scss" scoped>
    .footer {
        position: relative;
        z-index: 3;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-between;
        padding: 35px 40px;
        -webkit-box-shadow: 0px -4px 33px -15px rgba(0,0,0,0.36);
        -moz-box-shadow: 0px -4px 33px -15px rgba(0,0,0,0.36);
        box-shadow: 0px -4px 33px -15px rgba(0,0,0,0.36);

        h3 {
            text-transform: uppercase;
            color: #E1251B;
            letter-spacing: 1px;
            text-align: center;
            line-height: 1.3;
            margin: 25px 0;
        }

        ul.social {
            list-style-type: none;

            li {
                display: inline-block;
                margin: 0 10px;
            }
        }
    }

@media screen and (min-width: 768px) {
    .footer {
        flex-direction: row;
        padding: 35px 40px;

        img.logo {
            width: 25%;
        }

        h3 {
            font-size: 14px;
            width: 30%;
        }
        
        ul.social {
            li {
                margin: 0 5px;
                img {
                    width: 60%; 
                }
            }
        }
    }
}

@media screen and (min-width: 1024px) {
    .footer {
        h3 {
            width: 40%;
            font-size: 20px;
        }

        ul.social {
            li {
                margin: 0 10px;

                img {
                    width: 80%;
                }
            }
        }
    }
}

</style>