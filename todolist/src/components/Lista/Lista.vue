<template>
  <div>    
    <form action="">
      <div>
        <label for="titulo">Titulo</label><br>
        <input type="text" v-model="titulo" id="titulo">
        {{this.titulo}}
      </div>
      <div>
        <label for="titulo">Descrição</label><br>
        <input type="text" v-model="descricao" id="descricao">
      </div>
      <button type="button" class="btn-default" @click="addItem()">Adicionar</button>
    </form>
    <hr>
    <table>
      <thead>
        <tr>
          <td>Numero</td>
          <td>Titulo</td>
          <td>Ações</td>
        </tr>
      </thead>
      <tbody id="tbody">

      </tbody>
    </table>
  </div>
 
</template>

<script>
export default {
  data(){
    return {
      lista: [],
      titulo : '',
      descricao : ''
    }
  },
  props: {
    
  },
  methods: {
    addItem(){
      if(this.titulo.length == 0 || this.descricao.length == 0)
        alert('Titulo e descrição devem ser preenchidos');
      else{
        this.lista.push({titulo: this.titulo, descricao: this.descricao});
        this.titulo = '';
        this.descricao = '';
        this.atualizaTbody();
      }
      
    },
    atualizaTbody(){
      var html = '';
      this.lista.forEach(item => {
        html += '<tr><td>'+item.titulo+'</td> <td>'+item.descricao+'</td><td><button class="btn-danger">Excluir</button></td></tr>'
      });
      console.log(html);
      document.getElementById("tbody").innerHTML = html;
    }    
  }
}
</script>

<style>

.btn-default{
  margin-top:10px;
  font-size: 20px;
  background-color: rgb(0, 16, 160);
  color: rgb(255, 255, 255);
  border-radius: 5px;
  border-style: solid;
  border-color: rgb(0, 16, 160);
}
.btn-default:hover{  
  background-color: rgb(255, 255, 255);
  color: rgb(0, 16, 160);
}

.btn-danger{
  margin-top:10px;
  font-size: 20px;
  background-color: rgb(255, 0, 0);
  color: rgb(255, 255, 255);
  border-radius: 5px;
  border-style: solid;
  border-color: rgb(255, 0, 0);
}
.btn-danger:hover{
  background-color: rgb(255, 255, 255);
  color: rgb(255, 0, 0);
}


table{
  border: solid 1px;
  font-size: 25px;
  border-radius: 5px;
}
tr{
  border-bottom: 1px;
}
td{
  border-right: solid 1px;
  padding: 5px;
  color:black;
}
</style>
