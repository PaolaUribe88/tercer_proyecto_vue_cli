<template>
    <div id="componentesAvanzados">
        <h1>{{title}}</h1> 
        <img v-for="image in images_src" :key="image" :src="image" alt="">
        <p>{{ pepito }}</p>
    </div>
</template>
<script>
export default{
    name: 'Componentes_Avanzados',
    props:{ 
        title:{ 
            type:String, 
            default:"Mi titulo por default" 
        }, 
        images_src:{ 
            type: Array, 
            required:true, 
        },
        pepito:{
            type: String,
            default:'Valor Pepito',
            required:true,
        }
    },
    methods:{

    }

}
</script>
<style scoped>
    div{ 
        border: 3px solid rgb(37,86,150); 
        border-radius:10px; 
        padding:10px; 
        width:80%;
         margin:0 auto; 
         background-color:rgb(58,136,226); 
         color:white; 
         } 
    img{ 
        display:inline-block; 
        width: 30%;
        border-radius:50%; 
        margin-right: 10px; 
        border:3px solid rgb(19,62,143); 
        }
</style>