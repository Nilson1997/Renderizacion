<template>
<div>
    <navbar></navbar>
    <div class="content">
    <Siderbar></Siderbar>
    <div v-if='Math.random()>0.3'>
        <p>HOLA!!!!!!</p>
       <button class="botoncancelar">cancelar</button>
    </div>
    </div>
    <Footer class="contentfooter"></Footer>
</div>
</template>
<style >

.contentfooter{
    display: flex;
    margin-top:600px;
}
</style>
<script>
import Siderbar from '../components/Siderbar.vue'
import Navbar from '../components/Navbar.vue'
import Footer from '../components/Footer.vue'
import axios from 'axios'
export default{
    data(){
        return{
        }
    },
    methods(){
        
    },
    computed:{
    },
    components:{
        Siderbar,
        Navbar,
        Footer
    },
    mounted() {  
        axios.get("https://jsonplaceholder.typicode.com/posts").then(response=>{
            console.log(response.data)
        })
    },
}
</script>