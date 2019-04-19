<template>
    <div>
        账号:<input type="text" placeholder="请输入账号"><br>
        密码:<input type="text" placeholder="请输入密码"><br>
        <button @click="handlelogin()">登陆</button>
    </div>
</template>

<script>
export default {
    methods:{
        handlelogin(){
            this.$router.push("/home")
        }
    }
}
</script>

<style scoped>
    
</style>