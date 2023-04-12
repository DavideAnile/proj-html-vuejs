<script>
import FormSection from './FormSection.vue';
import CourseInfoSection from './CourseInfoSection.vue';

export default {
    data(){
        return{

            number : "1-800-555-555"

        }
    },

    components : {
        FormSection,
        CourseInfoSection,
    }
}

</script>

<template>

<FormSection :number="number"></FormSection>

<CourseInfoSection></CourseInfoSection>

</template>

<style lang="scss" scoped>


</style>