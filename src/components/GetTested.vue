<template>
    <div class="gettested">
        <div class="testtext">
            <h3>Got HIV?</h3>
            <h2>Only way to know is to</h2>
            <h1>Get Tested</h1>

            <b-button class="button">Find Clinics</b-button>
        </div>

        <div class="testimage">
            <img src="@/assets/gettreated.svg" alt="Female HIV Doctor">
        </div>
    </div>
</template>

<script>
    export default {
        name: "gettested"
    }
</script>

<style lang="scss" scoped>
.gettested {
    display: flex;
    flex-direction: column;
    background-color: #FF5100;
    padding: 40px 40px 50px 40px;

    .testtext {
        text-align: left;
        color: white;
        margin-bottom: 30px;

        h3 {
            text-transform: uppercase;
        }

        h1 {
            margin-top: 5px;
        }

        .button {
            margin-top: 15px;
            padding: 5px 25px;
            background-color: $yellow;
            border: none;
            color: $red;
            font-family: $Nunito;
        }
    }

    .testimage {
        text-align: center;
        img {
            width: 40%;
    
        }
    }
}

@media screen and (min-width: 768px) {
    .gettested {
        flex-direction: row;
        align-items: center;
        justify-content: center;

        .testtext {
            order: 2;
            margin-bottom: 0;
            margin-left: 30px;
        }

        .testimage {
            order: 1;
            img {
                width: 60%;
            }
        }
    }
}

@media screen and (min-width: 1024px) {
    .gettested {
        .testtext {
            h1 {
                font-size: 80px!important;
                line-height: 80px!important;
            }
        }
    }
}
</style>