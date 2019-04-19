<template>
    <div>
        <img src="" alt="">
        <button @click="handleto()">继续报障</button>
        <button @click="handletoto()">查看故障单</button>
    </div>
</template>
<script>
export default {
    methods:{
        handleto(){
            this.$router.push("/home")
        },
        handletoto(){
            this.$router.push("/record")
        }
    }
}
</script>
<style scoped>
    
</style>