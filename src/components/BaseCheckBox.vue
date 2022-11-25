<template>
    <input 
    type="checkbox"
    :checked ="modelValue"
    @change="$emit('update:modelValue', $event.target.checked)"
    class ="field"
    />
    <label >{{label}}</label>
</template>
<script>
    export default {
        props :{
            modelValue : {
                type : Boolean,
                default : false
            }, 
            label : {
                type :String ,
                default : ""
            }
        }
    }
</script>