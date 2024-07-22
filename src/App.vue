<script setup>
  import BoxFormulario from './components/BoxFormulario.vue';

  const validacao = ref(false);

  
  
  /* const contador = ref(0);

   function mostrarResultado() {
  if (confirmarSenha != senha || !email.includes("@") || senha == '') alert("Credenciais inválidas ou campos não prenchidos!");
  else {
    contador.value++;
    console.log("qe");

    if (contador.value < 2) validacao.value = true;
    else {
      validacao.value = false
      contador.value = 0
    }
  } 
}*/

</script>

<template>
  <div class="titulo">
    <h1>Formulário de Cadastro de Produtos</h1>
  </div>
  
  <box-formulario />
  

    <div v-if="validacao === true" class="resultado">
      <h2>Resultado</h2>
      <p>Nome: {{ nome }}</p>
      <p>Email: {{ email }}</p>
      <p>Senha: {{ senha }}</p>
      <p>Estado: {{ estado }}</p>
      <p>Cidade: {{ cidade }}</p>
      <p>Endereço: {{ endereco }}</p>
      <p>Hobbies: {{ hobbie }}</p>
      <p>Linguagem de programação: {{ linguagemProgramacao }}</p>
      <p>Biografia: {{ biografia }}</p>
    </div>
  
</template>

<style scoped>

  .titulo {
    text-align: center;
    padding: 3rem 0;
  }

  .formulario, .resultado {
    width: 48%;
    border-radius: 10px;
    padding: 20px;
    margin: 0 0 5rem;
  }

  .resultado {
    background-color: #dac2eb;
  }

</style>
