<script>
import FormSection from './FormSection.vue';
import CourseInfoSection from './CourseInfoSection.vue';
import CardsSection from './CardsSection.vue';
import Testimonials from './Testimonials.vue';
import News from './News.vue';

export default {
    data(){
        return{

            number : "1-800-555-555"

        }
    },

    components : {
        FormSection,
        CourseInfoSection,
        CardsSection,
        Testimonials,
        News,
    }
}

</script>

<template>

<FormSection :number="number"></FormSection>

<CourseInfoSection></CourseInfoSection>

<CardsSection></CardsSection>

<Testimonials></Testimonials>

<News></News>

</template>

<style lang="scss" scoped>


</style>