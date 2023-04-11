<script>
export default {
    data(){
        return{

            title : "Get Behind The Wheel",

            formTitle: "First Lesson Free!"

        }
    },

    props : {

        number : String
    }
}

</script>

<template>

    <div class="up-section my-container">
        <div class="text-container">
            <h2> {{ title }}</h2>
            <p id="first-paragraph">Lorem ipsum dolor sit amet consectetur adipisicing elit. Provident suscipit fugit atque et blanditiis odio similique sequi alias ipsa qui quod excepturi officiis vero debitis minima quos, quidem quasi! Sit.</p>
            <p id="second-paragraph">Lorem ipsum dolor sit amet consectetur adipisicing elit. Saepe, ullam earum itaque similique tenetur rerum ut, ea illum eaque accusantium reprehenderit harum? Amet eos sapiente, assumenda molestias facilis blanditiis illo? Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam quis doloremque maiores dolorum. Sed animi incidunt beatae excepturi, ex optio ullam consectetur, omnis nihil dolores dolorem error aperiam, necessitatibus fuga?</p>
        </div>

        <div class="form-container">
            <h2>{{ formTitle }}</h2>
            <div>When you make a block booking with us your first lesson is included free.</div>
            <input type="text" placeholder="Your Name*">
            <input type="email" placeholder="Email*">
            <input type="number" placeholder="Telephone">
            <input type="text" placeholder="Location">
            <div><button>request a callback</button></div>
        </div>

    </div>
    
    
    <div class="bottom-section my-container">
        <div id="left-bottom">
            <h2>Start Learning to Drive Today</h2>
            <div>Give us a call to schedule your first driving lesson</div>
        </div>

        <div id="right-bottom"><i class="fa-solid fa-phone-flip"></i> {{ number }}</div>
    </div>


</template>

<style lang="scss" scoped>

    .up-section{
        position: relative;
        display: flex;
        padding-bottom: 100px;
        
    
        

        .text-container{
            display: flex;
            flex-flow: column nowrap;
            gap: 20px;
            width: 45%;
            padding-top: 80px;

            #first-paragraph{
                line-height: 2em;
                opacity: .5;
                font-size: 1em;
            }

            #second-paragraph{
                line-height: 2em;
                opacity: .5;
                font-size: .8em;
            }
        }

        .form-container{
            position: absolute;
            top: -50px;
            right: 400px;
            
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            align-items: center;
            gap: 30px;
           
            padding: 30px 20px;
            border-radius: 10px;
            background-color: white;
            box-shadow: 4px 10px 30px lightgray;


            h2{
                color: #7abc64;
            }

            input{
                width: 100%;
                padding: 10px;
                background-color: rgba(211, 211, 211, 0.774);
                border: 1px solid lightgray;
            }

            div button{
                background-color: #7abc64;
                color: white;
                text-transform: uppercase;
                padding: 10px 20px;
                border-radius: 20px;
                border: none;
            }
        }
    }

    .bottom-section{
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 200px;
        background-image: url("/images/horizontal-cta-background.jpg");
        background-size: cover;
        background-position: center;
        color: white;

        #left-bottom{
            display: flex;
            flex-direction: column;
            gap: 20px;

            h2{
                font-size: 2em;
            }
        }

        #right-bottom{
            font-size: 1.5em;
            padding-right: 50px;
        }
    }

</style>