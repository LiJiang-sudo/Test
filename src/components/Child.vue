<template>
    <div>
        <h2>Child子组件部分</h2>
        <p>{{msg}}</p>
        <button v-on:click="sendMsg">向父组件传值</button>
    </div>
</template>
<script>
export default {
    props:['msg'],
    methods:{
        sendMsg:function(){
            this.$emit("father",'去微软推哦怕');
        }
    }
}
</script>