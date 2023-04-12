<script>
import FormSection from './FormSection.vue';
import CourseInfoSection from './CourseInfoSection.vue';
import CardsSection from './CardsSection.vue';
import Testimonials from './Testimonials.vue';

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
    }
}

</script>

<template>

<FormSection :number="number"></FormSection>

<CourseInfoSection></CourseInfoSection>

<CardsSection></CardsSection>

<Testimonials></Testimonials>

</template>

<style lang="scss" scoped>


</style>