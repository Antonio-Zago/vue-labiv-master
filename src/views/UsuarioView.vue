<template>
  <div class="usuario">
    <p>Palmeiras não tem mundial</p>
    <p v-if="nome.length > 5">{{nome}}</p>
    <p><input type="text" v-model="nome"></p>
    <ul >
      <li v-for="(anotacao,i) in anotacoes " :key="i">{{anotacao}}</li>
    </ul>
    <button @click="inserirUsuario">Ok</button>
  </div>
</template>

<script>

export default{
  name:'UsuarioView',
  data(){
    return {
      nome: 'teste',
      anotacoes:['oi', 'tchau', 'adfa']
    }
  },
  methods:{
    inserirUsuario(){
      this.anotacoes.push(this.nome)
      this.nome = ''
    }
  }
}
</script>
