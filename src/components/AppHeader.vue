<script>
export default {
    data(){
        return{
            number : "1-800-555-555",

            percentage : "95%",

            links : [
                "home",
                "about",
                "prices",
                "courses",
                "locations",
                "blog"
            ],

            title : "Drive with Avada"

        }
    }
}

</script>

<template>
<div class="header-section">
    
        <div class="up-header my-container">
            <div>We have a {{ percentage }} Successful Pass Rate!</div>
            <div><i class="fa-solid fa-phone-flip"></i> Give us a call to book your tuition! {{ number }}</div>
        </div>
        <div class="bottom-header">
            <div class="jumbo-container">
                <img src="/images/homepage-hero-background.jpg" alt="">

                <div class="up-container my-container">
                    <div class="logo-container">
                        <img src="/images/avada-drivers-logo-1x.png" alt="">
                    </div>
                    <div class="links-container">
                        <li v-for="link in links"><a href="#">{{ link }}</a></li>
                    </div>
                    <div class="btn-container">
                        <button>book now</button>
                    </div>
                </div>

                <div class="center-container my-container">
                    <div><h1>{{ title }}</h1></div>
                    <div>We offer the finest driving tuition money can buy</div>
                </div>

                <div class="right-up-container">
                    <div id="demos"><i class="fa-solid fa-folder-open"></i> <span> Demos </span> </div>
                    <div id="sales"> <span id="price"> <small>$</small> 39 </span> <span> On Sale </span> </div>
                </div>
                        

            </div>
        </div>
    

</div>
</template>

<style lang="scss" scoped>

.header-section{
    width: 100%;
    height: 700px;
    

    .up-header{
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;
        height: 8%;
        background-color: #353637;
        color: rgba(211, 211, 211, 0.733);
        
    }

    
    .bottom-header{
        position: relative;
        width: 100%;
        height: 92%;

        .jumbo-container{
        position: relative;
        height: 100%;
        

            img{
                width: 100%;
                
               
                
            }
            
            .up-container{
                position: absolute;
                top: 0;
    
                display: flex;
                justify-content: space-between;
                align-items: center;
                
                
                width: 100%;
                height: 100px;
                background-color: #35363773;
                
    
                .logo-container{
                    height: 100%;
                    padding: 25px 0 ;
                    
                    
                    img{
                        height: 100%;
                    }
                }
    
                .links-container{
                    display: flex;
                    gap: 40px;
                    list-style-type: none;
    
                    li {
                        
                        a{
                            text-decoration: none;
                            color: white;
                            text-transform: uppercase;
                            font-weight: bold;
                            padding: 10px 0;
                            transition: .1s;
                            
                        }
                          
                        a:hover{
    
                            color: #7abc64;
                            border-bottom: 2px solid #7abc64;
                            
                        }
    
                    }
                        
                    li:nth-child(4)::after{
                        content: "NEW";
                        color: white;
                        font-weight: bold;
                        margin-left: 10px;
                        font-size: .8em;
                        padding: 3px;
                        background-color: #7abc64;
                        border-radius: 5px;
    
                        
                    }   
    
                }
                
                .btn-container{
                    padding: 15px;
                    
                    button{
                        padding: 10px 20px;
                        background-color: #7abc64;
                        border: none;
                        text-transform: uppercase;
                        font-weight: bold;
                        color: white;
                        border-radius: 20px;
                        cursor: pointer;
                    }
                }
                    
                .btn-container:hover{
                    background-color: #7abc6479;
                    cursor: pointer;
                }
    

            }
    
            .center-container{
                position: absolute;
                top: 50%;
                
    
    
                display: flex;
                flex-direction: column;
                gap: 10px;
    
                height: auto;
                color: rgba(255, 255, 255, 0.822);
                font-size: 1.5em;
            }
    
            img{
                display: block;
                height: 100%;
                
            }
    
            .right-up-container{
                position: absolute;
                top: 85px;
                right: 10px;
    
    
    
                display: flex;
                flex-direction: column;
                align-items: center;
                gap: 10px;
                width: 60px;
                cursor: pointer;
                
    
               
                 #demos{
                    display: flex;
                    flex-direction: column;
                    align-items: center;
                    
                    background-color: white;
                    padding: 6px;
                    width: 100%;
                    height: 60px;
                    border-radius: 10px;
    
                    i{
                        font-size: 2em;
                        color: rgb(2, 2, 75);
                    }
    
                 }   
    
                #sales{
                    position: relative;
                    display: flex;
                    flex-direction: column;
                    align-items: center;
    
                    background-color: white;
                    padding: 6px;
                    width: 100%;
                    height: 60px;
                    font-size: .7em;
                    font-weight: bold;
                    border-radius: 10px;

                    small{
                        position: absolute;
                        top: 2px;
                        left: 6px;
                        font-size: .8em;
                    }
    
                    #price{
                        font-size: 2em;
                        font-weight: bold;
                        color: #7abc64;
                    }
    
                } 
                 
            }
            
        }
        
    }

}
</style>

        

                
                    




                
            
            
            

