<script setup>
import { ref } from 'vue';
import BoxFormulario from './components/BoxFormulario.vue';
import BoxResultado from './components/BoxResultado.vue';
const perfil = ref({ nome: '' });
const validacao = ref(false);

function enviarItem(item) {
  Object.assign(perfil.value, item);
  validacao.value = !validacao.value;
}

/* const validacao = ref(false);

  function mostrarResultado() {
    if (nome.value == '' || email.value == '' || senha.value == '' || confirmarSenha.value == '' || 
    endereco.value == '' || cidade.value == '' || estado.value == '' || hobbie.value == '' || 
    linguagemProgramacao.value == '' || biografia.value == '') {
      alert('Preencha todos os campos');
    }
    else {
      
      if (nome.value.length < 5) alert('Preencha seu nome corretamente');
      else if (!email.value.includes('@')) alert('Preencha seu email corretamente');
      else if (senha.value.length < 4) alert('Senha fraca');
      else if (confirmarSenha.value != senha.value) alert('Campo "Confirmar senha" preenchido incorretamente');
      else validacao.value = true;

    }
  } */
</script>

<template>
  <main class="conteudo">
    <div class="titulo">
      <h1>Formulário de Cadastro de Produtos</h1>
    </div>

    <BoxFormulario :validacao="validacao" @envio="enviarItem" />
    <BoxResultado :perfil="perfil" :validacao="validacao"/>
  </main>
  
</template>

<style scoped>
  main{
    display: grid;
    justify-items: center;
  }

  .titulo {
    text-align: center;
    padding: 3rem 0;
  }
</style>
