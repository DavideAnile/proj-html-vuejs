<script>
export default {
    data(){
        return{

            cards : [
                {
                    img : "/images/blog-choosecar-700x441.jpg",
                    title : "What Car to Start With?"
                },
                {
                    img : "/images/blogpost-10and2-700x441.jpg",
                    title : "Avada Driving School Expanding"
                }
            ]

        }
    }
}
</script>

<template>

<section class="news my-container">
    <div class="container">
        <h1>Latest News</h1>
        <div class="cards-container">
            <div v-for="card in cards" class="card">
                <div class="img-container">
                    <img :src="card.img" alt="">
                </div>
                <h2>{{card.title}}</h2>
                <small>February 7th 2019 | <small style="color: #7abc64; cursor: pointer;">0 Comments</small></small>
                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Repellendus, accusantium perferendis ipsa doloremque nobis, </p>
            </div>
        </div>
        <div class="btn-container"><button>more from the blog</button></div>
    </div>
    <div id="bottom-container-triangle"><img src="/images/latestnews-bottom.png" alt=""></div>
</section>

</template>

<style lang="scss" scoped>

.news{
background-image: url("/images/latestnews-background.jpg");
background-size: cover;

    .container{
        position: relative;
        top: -30px;
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 20px;
        border-top: 5px solid #7799ad;
        border-top-right-radius: 10px;
        border-top-left-radius: 10px;
        padding: 20px;
        background-color: white;
        box-shadow: 4px 10px 30px black;
        
    
        h1{
            padding: 30px 0 ;
            font-size: 2em;
            
        }
    
        .cards-container{
            display: flex;
            
            .card{
                display: flex;
                flex-direction: column;
                align-items: center;
                text-align: center;
                color: gray;
    
                .img-container{
                    width: 500px;
                    height: 300px;
                    margin-bottom: 30px;
                    cursor: pointer;
                   
    
                    img{
                        width: 100%;
                        height: 100%;
                        object-fit: cover;
                    }
                }
    
                h2{
                    color: #7abc64;
                    padding: 5px;
                }
    
                p{
                    padding: 30px;
                    line-height: 1.7em;
                }
            }
        }

        .btn-container{

            button{
                padding: 10px 30px;
                border-radius: 20px;
                border: none;
                text-transform: uppercase;
                background-color: #7abc64;
                color: white;
                transition: .7s;
            }

            button:hover{
                transform: scale(1.2);
                cursor: pointer;
            }
        }

    }
        
    #bottom-container-triangle{
            position: relative;
            top: -30px;
            width: 100%;
            
            img{
                width: 100%;
            }
            
    }

}



</style>