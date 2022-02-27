<script>
export default{
    data(){
        return{
        isPurple:false,
        isRed:false,
        selectedColor:''
        }
    },
    computed:{
        circleClasses(){
            return {red:this.isRed}
        }
    }
}
</script>
<template>
<label>
<input type="checkbox" v-model="isRed"/>red

</label>
<select v-model="selectedColor">
<option>white</option>
<option value="text-black">black</option>
<option value="text-orange">orange</option>
</select>
<div class="circle" :class="[selectedColor,circleClasses]">hi</div>
</template>
<style src="../assets/main.css" scoped>
</style>
