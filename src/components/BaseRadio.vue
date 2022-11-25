<template>
    <input
        type="radio"
        v-model="event.pets"
        :value="value"
        :checked ="modelValue === value"
        @change ="$emit('update: modelValue', value)"
        v-bind ="$attrs"
    />
</template>
<script>
    export default {
        props: {
            label : {
                default : "",
                type : String
            },
            modelValue : {
                type : [String, Number],
                default : ""
            },
            value : {
                type : [String, Number],
                required : true,

            }
        }
    }
</script>