<script>
export default {
    data(){
        return{
            

            people : [
                {
                    img : "/images/testimonial-sophia.png",
                    name : "Sophia Jones",
                    text : "Avada Driving School really helped build my confidence behind the wheel and with driving in general Higly recommended.",
                },
                {
                    img : "/images/testimonial-grant.png",
                    name : "Grant Smith",
                    text : " confidence behind the wheel and with driving in general, and they got me a first time pass! Higly recommended.",
                },
                {
                    img : "/images/testimonial-harold.png",
                    name : "Harold Stevenson",
                    text : "driving in general, and they got me a first time pass! Higly recommended. i'm sure that many people must be interested about that experience!",
                },
                {
                    img : "/images/testimonial-kelly.png",
                    name : "Kelly Manson",
                    text : "Avada Driving School really helped build my confidence behind time pass! Higly recommended. To be honest it's the best!",
                },
                {
                    img : "/images/testimonial-kate.png",
                    name : "Kate Wotsbolo",
                    text : "Avada Driving School really helped build my confidence behind the wheel and with driving in general, and they got me a first time pass! Higly recommended.",
                }
            ],

            activeIndex : 0
        }
    },

}
</script>

<template>

<section class="section-container my-container">

    <div class="up-section">
        <div id="title">Testimonials</div>
        <p>Here's what our happy drivers had to say about our services :</p>
    </div>
    <div class="bottom-section">
        <div class="img-container">
            <img :src="people[activeIndex].img" alt="">
        </div>
        <p><em>{{ people[activeIndex].text }}</em></p>
        <div class="person-name"> {{ people[activeIndex].name }}</div>
        <div class="dots-container">
            <div v-for="(person, indice) in people" class="dot" :class="activeIndex == indice ? 'active' : '' " @click="activeIndex = indice"></div>
        </div>
    </div>

</section>

</template>

<style lang="scss" scoped>

.section-container{
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 50px;
    color: gray;
    background-image: url("/images/testimonial-background.jpg");
    background-size: cover;
    background-position: center;
    padding: 150px 0;

    .up-section{
        display: flex;
        flex-direction: column;
        align-items: center;

        #title{
            font-size: 2em;
            font-weight: bold;
            padding: 20px;
            color: rgba(0, 0, 0, 0.555)
        }
    }

    .bottom-section{
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 20px;

        .img-container{
            width: 100px;
            height: 100px;
            
            border-radius: 100%;
            

            img{
                width: 100px;
            }
        }

        p{
            letter-spacing: 2px;
            text-align: center;
            line-height: 2em;
            padding: 0 500px;
            
        }

        .person-name{
            font-weight: bold;
            font-size: 1.2em;
            color: rgba(0, 0, 0, 0.555);
        }

        .dots-container{
            display: flex;
            gap: 7px;

            .dot{
                width: 20px;
                height: 20px;
                border: 1px solid gray;
                border-radius: 100%;
                cursor: pointer;
                
            }

            .dot.active{
                background-color: gray;
            }
            
        }
    }
}

</style>