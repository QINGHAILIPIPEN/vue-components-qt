<template>
    <h3>Parent</h3>
    <!-- <Child title="Parent数据"/> -->
    <Child :title="message" :age="age" :names="names" :userInfo="userInfo"/>
</template>
<script>
import Child from './Child.vue';
export default {
    data(){
        return{
            message:"Parent数据！",
            age:20,
            names:["iwen","ime","frank"],
            userInfo:{
                name:"iwen",
                age:18
            }
        }
    },
    components:{
        Child
    }
}
</script>