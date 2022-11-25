<template>
    <component 
        v-for="option in options"
        :key ="option.value"
        :is="vertical ? 'div' : 'span'">
            <BaseRadio 
            
            :label ="option.label"
            :value="option.vaule"
            :name ="name"
            :modelValue="modelValue"
            @update:modelValue="$emit('update:modelValue',$event)"
            :class ="{
                horizontal : !vertical
            }"
        />
    </component>
    
</template>
<script>
import BaseRadio from './BaseRadio.vue';

    export default {
    props: {
        options: {
            type: Array,
            requried: true,
        }, 
        name :{
            type : String, 
            required : true
        },
        modelValue :{
            type : [Number, String],
            required : true
        }, 
        vertical : {
            type : Boolean,
            default : false 

        }
    },
    components: { BaseRadio }
}
</script>

<style>
    .horizontal {
        margin-left: 20px;
    }

</style>