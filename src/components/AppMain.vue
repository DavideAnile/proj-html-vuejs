<script>
import FormSection from './FormSection.vue';

export default {
    data(){
        return{

            number : "1-800-555-555"

        }
    },

    components : {
        FormSection,
    }
}

</script>

<template>

<FormSection :number="number"></FormSection>

</template>

<style lang="scss" scoped>


</style>