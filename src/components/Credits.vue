<script>
export default {
    data(){
        return{

            img : "/images/avada-drivers-logo-1x.png",
            text : "Avada Driving School is the right choice for experienced drivers looking for a refresher course, or the brand new driver wanting to pass first time",

            details : {

                title :  "contact detail",
                address :  "12345 North Main Street, New York, NY 55555",
                number :  "1.800.555.6789",
                email : "info@your-domain.com",
                site : "Theme-Fusion.com"
            },

            links : [

                
                "Pass Plus",
                "Intensive Course",
                "Automatic",
                "Instructor Training"

            ]

        
            

        }
    }
}
</script>

<template>

    <section class="up-section my-container">
        <div class="left-footer">
            <div class="logo-container">
                <img :src="img" alt="">
            </div>
            <p>{{ text }}</p>
        </div>
        <div class="details">
            <div class="title">{{ details.title }}</div>
            <div class="detail">
                <div><i class="fa-solid fa-house-chimney"></i></div>
                <div> <a href="">{{ details.address }}</a></div>
            </div>
            <div class="detail">
                <div><i class="fa-solid fa-phone-flip"></i></div> 
                <div><a href="">{{ details.number }}</a></div>
            </div>
            <div class="detail">
                <div><i class="fa-solid fa-envelope"></i></div> 
                <div><a href="">{{ details.email }}</a></div>
            </div>
            <div class="detail">
                <div><i class="fa-solid fa-link"></i></div> 
                <div><a href="">{{ details.site }}</a></div>
            </div>
        </div>
        <div class="links">
            <div class="title">courses</div>
            <ul>
                <li v-for="link in links"><i class="fa-solid fa-circle-arrow-right"></i> <a href="#">{{ link }}</a> </li>
            </ul>
        </div>
        <div class="right-footer">
            <div class="img-container">
                <img src="/images/footer-ad-grid.png" alt="">
            </div>
            <div class="btn-container"><button>BOOK NOW</button></div>
        </div>

    </section>

    <section class="bottom-section my-container">
        <div class="left-container">
            <small><i class="fa-regular fa-copyright"></i> Copyright 2012 - 2020 | Avada Theme by <span><a href="#">ThemeFusion</a></span> | All Rights Reserved | Powered by <span><a href="#">Wordpress</a></span></small>
        </div>
        <div class="right-container">
            <i class="fa-brands fa-facebook-f"></i>
            <i class="fa-brands fa-twitter"></i>
            <i class="fa-brands fa-youtube"></i>
            <i class="fa-brands fa-instagram"></i>
        </div>
    </section>

</template>

<style lang="scss" scoped>

.up-section{
    display: flex;
    justify-content: space-between;
    color: rgba(211, 211, 211, 0.60);
    background-image: url("/images/footer-background-color.jpg");
    background-size: cover;
    padding-top: 80px;

    .left-footer{
        width: 25%;

        p{
            padding: 10px 0;
            line-height: 2em;
        }
    }

    .details{
        display: flex;
        flex-direction: column;
        gap: 20px;
        width: 25%;

        .title{
            color: white;
            font-weight: bold;
            text-transform: uppercase;
        }
        .detail{
            display: flex;
            gap: 20px;
            
            a{
                text-decoration: none;
                color: rgba(255, 255, 255, 0.6);
            }

            a:hover{

                text-decoration: underline;
            }
        }
    }

    .links {
        color: #7abc64;

        .title{
            text-transform: uppercase;
            color: white;
            font-weight: bold;
        }

        ul{
            display: flex;
            flex-direction: column;
            gap: 25px;
            list-style-type: none;
            padding-top: 20px;

            li{
                a{
                    text-decoration: none;
                    color: #7abc64;
                }

                a:hover{
                    text-decoration: underline;
                }
            }
        }
    }

    .right-footer{
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 30px;
        width: 25%;
        margin-bottom: 40px;

        .img-container{
            width: 100%;
            cursor: pointer;
            

            img{
                width: 100%;
            }
        }
        
        .btn-container{
            padding: 15px 20px;
            transition: .7s;
            
            button{
                padding: 10px 20px;
                border-radius: 20px;
                border: none;
                background-color: #7abc64;
                color: white;
                cursor: pointer;
            }

        }

        .btn-container:hover{
            transform: scale(1.1);
            background-color: #7abc644d;
            cursor: pointer;
        }
    }
}

.bottom-section{
    display: flex;
    justify-content: space-between;
    padding-top: 50px;
    padding-bottom: 50px;
    color: gray;
    background-color: #1c1d1e;

    .left-container{

        span{
            
            a{
                text-decoration: none;
                color: #7abc64;
            }

            a:hover{
                text-decoration: underline;
            }
        }
            
    }
    .right-container{
        display: flex;
        gap: 15px;
        color: white;

        i{
            transition: .6s;
        }

        i:hover{
            transform: scale(1.5);
            cursor: pointer;
        }
    }
    
}


</style>