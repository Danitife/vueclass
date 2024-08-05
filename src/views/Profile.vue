<template>
    <div>
        <h1 class="text-2xl">This is {{ username }} profile page</h1>
        <h1 class="tw-bg-yellow-700 text-primary">Your email is {{ email }}</h1>
        <h1 class="bg-yellow-700 text-1">Your email is {{ email }}</h1>
        <h1 class="bg-yellow-700 text-3">Your email is {{ email }}</h1>
        <button @click="changeName()" class="btn btn-primary">Click me</button>
        <div :class="lightOn? 'tw-bg-yellow-500 tw-w-[200px] tw-h-[200px]': 'tw-bg-black tw-w-[200px] tw-h-[200px]'">uytrdfgh</div>
        <button class="btn btn-info" @click="switchLight()">{{ lightOn? "Off Light": "On Light" }}</button>

    </div>
    <img src="/img/title_here.png" alt="">
</template>


<script>
export default {
    data(){
        return{
            username: "Samuel",
            email: "daniel@gmail.com",
            lightOn: false
        }
    },
    mounted() {
        alert("Hello") 
    },
    methods:{
        changeName(){
            this.username == "Samuel"? this.username = "Victor" : this.username= "Samuel"
        },
        switchLight(){
            this.lightOn = !this.lightOn
        }
    }
}
</script>
<style lang="">
    
</style>