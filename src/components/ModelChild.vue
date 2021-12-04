<template>
    <div>
        <button @click="sendMsg">点击发送message</button>
    </div>
</template>
<script>
export default {
    props:{
        modelValue:{},
        'first-name':{
            type:String,
        },
        'last-name':{
            type:String,
        },
    },
    methods:{
        sendMsg(){
            this.$emit("update:modelValue",Math.random())
            this.$emit("update:first-name","chen")
            this.$emit("update:last-name","shimiao")
        }
    }
}
</script>