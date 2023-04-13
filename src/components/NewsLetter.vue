<script>
export default {
    data(){
        return{

            sectionTitle : "Sign up to our Newsletter",

            text : "(We do not share your data with anybody, and only use it for its intended purpose.)"

        }
    }
}
</script>

<template>

<section class="newsletter my-container">

    <h2>{{ sectionTitle }}</h2>
    <input type="text">
    <button>subscribe</button>
    <div>{{ text }}</div>

</section>

</template>

<style lang="scss" scoped>

.newsletter{
    display: flex;
    flex-direction: column;
    align-items: center;
    background-image: url("/images/newsletter_background.jpg");
    background-size: cover;

    h2{
        padding: 50px;
    }

    input{
        width: 100%;
        max-width: 500px;
        padding: 10px;
        margin-bottom: 20px;
        border: 1px solid lightgray;
        outline: none;
    }

    button{
        width: 100%;
        max-width: 500px;
        padding: 10px;
        border-radius: 20px;
        border: none;
        background-color:  #7abc64;
        color: white;
        text-transform: uppercase;
        transition: .7s;
    }

    button:hover{
        transform: scale(1.1);
        cursor: pointer;
    }

    div{
        padding: 40px;
    }
}

</style>