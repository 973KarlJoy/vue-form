<template>
 <label v-if="label"> {{label}}  </label>
 <select
    class ="field"
    :value ="modelValue">
    <option 
    v-for="option in categories"
    :value="option"
    :key ="option"
    :selected="option===event.category">{{option}}</option>
</select>
</template>
<script>
    export default {
        props : {
            label :{
                default : "",
                type : String,
            },
            modelValue : {
                default : "",
                type : [Number, String]
            }
        }

}
</script>