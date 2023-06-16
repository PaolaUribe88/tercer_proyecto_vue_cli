<template>
    <div id="galleryApp">
        <h1>{{ mensaje }}</h1>
       <button v-on:click="saludar">Saludo</button>
       <hr>
       <h2>{{ titulo }}</h2>
       <img v-for="image in images_src" v-bind:key="image" v-bind:src="image" alt="">
       <h3>{{ nombreImg }}</h3>
    </div>
</template>
<script>
    export default { 
        name:"galleryApp", 
        props:['titulo','images_src','nombreImg'] ,
        data: function(){
            return{
                mensaje: '',
                
            }
        },
        methods: {
            saludar: function(){
                this.mensaje = 'Este mensaje es parte del componente Hijo'
            },
        }
        
    }
</script>

<style scoped>
    div{ 
        border: 3px solid rgb(37,86,150); 
        border-radius:10px; 
        padding:10px; width:60%; 
        margin:0 auto; background-color:rgb(58,136,226); 
        color:white; 
    } 
    img{ 
        display:inline-block; 
        width: 40%;
        border-radius:50%; 
        margin-right: 10px;
        border: 3px solid rgb(194, 209, 236);
    }
</style>