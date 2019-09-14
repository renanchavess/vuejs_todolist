<template>
    <div class="barraTop">
        <nav>
            <a href="">Nova tarefa</a>
            <a href="">Lista de tarefas</a>
            <a href="">Tarefas concluidas</a>
        </nav>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>

    .barraTop{        
        background-color:rgb(0, 119, 255);
    }
    nav{
        padding: 20px 20px 20px 0px;
    }

    nav a{
        padding: 10px;
        text-decoration: none;        
        background-color: rgb(255, 255, 255);
        color: rgb(0, 16, 160);
        font-size: 20px;
        border-radius: 12.5px;
        margin-left: 5px;
        
    }
    
    nav a:hover{
        padding: 10px;
        text-decoration: none;
        background-color: rgb(0, 16, 160);
        color: rgb(255, 255, 255);
    }
</style>