<template>
    <h3>ComponentB</h3>
    <p>{{ title }}</p>
    <p>{{ age }}</p>
    <p v-for="(item,index) of names">{{ item }}</p>
    <button @click="updataHandle">修改数据</button>
</template>

<script>
    export default{
        data(){
        return{
            
        }
    },

        props:{
            title:{
                type:[String,Number,Array,Object],
                //必选项
                required:true
            },
            age:{
                type:Number,
                //默认值
                default:0
            },
            //数字和字符串可以直接default，但是如果是数组和对象，必须通过工厂函数返回默认值
            names:{
                type:Array,
                default(){
                    return ["空"]
                }
            }
        },
        methods:{
            updataHandle(){
                //错误操作，不允许修改父元素传递过来地数据
                this.title = "新数据"
                
            }
        }
    }
</script>