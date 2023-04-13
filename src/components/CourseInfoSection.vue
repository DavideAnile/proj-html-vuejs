<script>

export default {
    data(){
        return{

            cards : [
                {
                    img : "/images/courses-passplus.jpg",
                    title : "Pass Plus"
                },
                {
                    img : "/images/course-intensive.jpg",
                    title : "Intensive Course",
                },
                {
                    img : "/images/courses-instructor.jpg",
                    title : "Instructors"
                }
            ]

        }
    }
}

</script>


<template>

<div class="info-section my-container">
    <div class="big-card-container">
        <h2>Course</h2>
        <p>lorem ipsum dolor, nostrum consequuntur enim magnam officiis? Eum excepturi ad nihil modi voluptas cumque quis exercitationem explicabo dignissimos architecto.</p>
        <div><button>Course Information</button></div>
        <div id="corner"><img src="/images/new-corner.jpg" alt=""></div>
    </div>
    <div class="cards-container">
        <div v-for="card in cards" class="card">
            <div class="img-container"><img :src="card.img" alt=""></div>
            <h3>{{ card.title }}</h3>
            <div class="btn-container"><button>Learn more</button></div>
        </div>
        
    </div>
</div>

<div id="driving-triangle">
    <img src="/images/driving-triangle.svg" alt="">
</div>

</template>

<style lang="scss" scoped>

.info-section{
    position: relative;
    display: flex;
    gap: 20px;
    background-image: url("/images/promise-background.jpg");
    background-size: cover;
    background-position: center;

    .big-card-container{
        position: relative;
        top: -20px;
        
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 30px;
        width: 35%;
        
        background-color: white;
        padding: 40px 20px;
        border-radius: 10px;
        box-shadow: 4px 10px 50px rgba(0, 0, 0, 0.425);

        h2{
            font-size: 2em;
        }

        p{
            line-height: 2em;
            text-align: center;
            opacity: .5;
        }

        div button{
            padding: 10px 20px;
            border-radius: 20px;
            background-color: #7abc64;
            color: white;
            border: none;
            text-transform: uppercase;
            font-weight: bold;
            letter-spacing: 2px;
            transition: .5s;
        }

        div button:hover{
            transform: scale(1.1);
            cursor: pointer;
        }

        #corner{
            position: absolute;
            top: 0;
            left: 0;
            border-top-left-radius: 10px;
            overflow: hidden;
            height: 50px;

            img{
                height: 100%
            };
        }
        
    }

    .cards-container{
        display: flex;
        justify-content: space-around;
        flex-grow: 1;
        padding: 50px 10px;

        .card{
            display: flex;
            flex-direction: column;
            align-items: center;
            
            .img-container{
                width: 150px;
                height: 150px;

                img{
                    height: 100%;
                }
            }

            h3{
                text-align: center;
                padding: 20px 0;
                color: rgba(27, 27, 129, 0.418);
            }

            .btn-container{

                
                transition: .5s;
                
                
                button{
                    
                    padding: 7px 15px;
                    border: 2px solid rgba(27, 27, 129, 0.418);
                    border-radius: 20px;
                    color: rgba(27, 27, 129, 0.418);
                    text-transform: uppercase;
                    font-weight: bold;
                    transition: .5s;
                    letter-spacing: 2px;
                    cursor: pointer;
                }
            } 
                
            .btn-container:hover button{
                    color: #7abc64;
                    border: 2px solid #7abc64;
                    transform: scale(1.1);
            }    
            
        }
    }
}
            

#driving-triangle{
    width: 100%;
    
    img{
        width: 100%;
        opacity: .5;
        
    }
}


</style>