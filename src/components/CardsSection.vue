<script>


export default {
    data(){
        return{

            cards : [
                {   
                    img : "/images/instructor-mikehart.jpg",
                    name : "Mike Hart"
                },
                {
                    img : "/images/instructor-johnsmith.jpg",
                    name : "John Smith"
                },
                {
                    img : "/images/instructor-angelahart.jpg",
                    name : "Angela Hart"
                }
            ]

        }
    }
}

</script>

<template>

<section class="cards-section my-container">
    <div class="first-container">
        <div class="percentage-card">
            <div class="circle-border-pass">
                <div class="circle"> <span>95 %</span> </div>
            </div>
            <h3>Pass rate</h3>
        </div>
        <div class="percentage-card">
            <div class="circle-border-referral">
                <div class="circle"><span>100 %</span></div>
            </div>
            <h3>Referral rate</h3>
        </div>
        <div class="percentage-card">
            <div class="circle-border-accident">
                <div class="circle"> <span>0 %</span></div>
            </div>
            <h3>Accident rate</h3>
        </div>
    </div>
    <div class="second-container">
        <div class="left-container">
            <h2>Your instructors</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas vel dolorum suscipit illum ullam autem est labore accusamus corporis in odio, eos modi architecto veniam nihil ex, eveniet cum voluptates?</p>
        </div>
            
        <div class="right-container"><button>More about us</button></div>
    </div>
    <div class="third-container">
        <div v-for="card in cards" class="card">
            <div class="img-container">
                <img :src="card.img" alt="">
                <div class="hidden">{{ card.name }}</div>
            </div>
            <h3>{{card.name}}</h3>
            <div class="icons-container">
                <i class="fa-brands fa-facebook"></i>
                <i class="fa-brands fa-twitter"></i>
                <i class="fa-brands fa-instagram"></i>
            </div>
            <p> Aperiam nobis minima vero molestiae ipsum possimus ex veniam, numquam hic similique eius dolores.</p>
        </div>
        
    </div>

</section>


</template>

<style lang="scss" scoped>

@mixin cerchio() {
                    position: relative;
                    top: 5px;
                    left: 5px;

                    display: flex;
                    align-items: center;
                    justify-content: center;
                    
                    width: 100px;
                    height: 100px;
                    text-align: center;
                    border-radius: 100%;
                    background-color: #ffffff;
}

@mixin bordoCerchio () {

                    position: relative;
                    width: 110px;
                    height: 110px;
                    border-radius: 100%;

}

@mixin percentuale (){

                    font-size: 1.5em;
                    color: gray;
                    font-weight: bold;

}



.cards-section{
    display: flex;
    flex-direction: column;
    gap: 50px;

    .first-container{
        position: relative;
        top: -70px;
        
        display: flex;
        justify-content: space-between;

        h3{
            text-transform: uppercase;
            color: gray;
        }

        .percentage-card{
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 40px;
            width: 32%;
            padding: 70px 10px;
            border-top: 5px solid #7abc64;
            border-radius: 10px;
            box-shadow: 4px 10px 30px lightgray;
            background-color: white;
            

            .circle-border-pass{
                
                @include bordoCerchio();
                background: linear-gradient(270deg, #7abc64 50%, transparent 50%), linear-gradient(70deg, #7abc64 50%, lightgray 50%);
                .circle{
                    
                    @include cerchio();
                    
                    span{
                        @include percentuale();
                    }
                }
            }

            .circle-border-referral{
                @include bordoCerchio();
                background: linear-gradient(270deg, #7abc64 50%, transparent 50%), linear-gradient(90deg, #7abc64 50%, lightgray 50%);

                .circle{
                    @include cerchio();

                    span{
                        @include percentuale()
                    }
                }
            }
                
            .circle-border-accident{
                @include bordoCerchio();
                background: lightgray;
                .circle{
                    @include cerchio();
                    

                    span{
                        @include percentuale()
                    }
                }
            }    
                

        }
        
    }

    .second-container{
        display: flex;
        align-items: center;
        gap: 20px;

        .left-container{
            display: flex;
            flex-direction: column;
            gap: 30px;
            width: 75%;

            p{
                font-size: 1.1em;
                color: gray;
                line-height: 2em;
            }
        }

        .right-container{
            flex-grow: 1;

            button{
                width: 100%;
                padding: 10px 0;
                border-radius: 20px;
                border: none;
                color: white;
                background-color: #7abc64;
                text-transform: uppercase;
                transition: .7s;
            }

            button:hover{
                transform: scale(1.1);
                cursor: pointer;
            }
        }
    }

    .third-container{
        position: relative;
        bottom: -70px;
        display: flex;
        justify-content: space-between;

        .card{
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 20px;
            width: 30%;
            box-shadow: 4px 10px 30px gray;
            border-top: 5px solid #7abc64;
            border-radius: 10px;
            padding: 0 30px;
            color: gray;
            background-color: white;
            transition: .5s;

            .img-container{
                position: relative;
                display: flex;
                align-items: center;
                justify-content: center;
                
                width: 100%;
                height: 200px;
                padding: 30px;

                img{
                    height: 100%;
                }

                .hidden{
                    display: none;
                    position: absolute;
                    top: 40px;
                    right: 30px;
                    background-color: white;
                    color: black;
                    padding: 2px;
                    border: 1px solid black;
                }

            }

            h3{
                color: black;
            }

            .icons-container{
                display: flex;
                gap: 20px;
            }

            p{
                line-height: 2em;
                padding-bottom: 50px;
            }
        }

        .card:hover{
            transform: scale(1.2);
            cursor: pointer;
        }

        .card:hover .img-container .hidden{
            display: block;
        }
    }
}


</style>