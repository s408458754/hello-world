<template>
    <div>
        <slot name="header" :isMy="isMy"></slot>
        <slot name="container"></slot>
    </div>
</template>
<script>
export default {
    data(){
        return {
            isMy:'我是子组件的变量isMy'
        }
    }
}
</script>