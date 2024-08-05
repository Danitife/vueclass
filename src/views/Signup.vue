<template>

    <div v-for="items in details">
        <p>{{ items }}</p>
    </div>
    <form action="">
        <input v-model="first_name" class="d-block py-[5px] my-[5px]" type="text" placeholder="First Name">
        <input class="d-block py-[5px] my-[5px]" type="text" placeholder="Last Name">
        <input class="d-block py-[5px] my-[5px]" type="email" placeholder="Email">
        <button @click="register()">Register</button>
    </form>

</template>

<script>
    export default{
        data(){
            return{
                first_name: "",
                allUser: [],
                details: ["Man", "Woman", "He", "She"]
            }
        },
        mounted(){

        },
        methods:{
            register(){
                console.log(this.first_name);
                this.allUser.push(this.first_name);
                localStorage.setItem("allUser", JSON.stringify(this.allUser))
            }
        }
     
    }
</script>