<template>
    <section class="newsletter">
      <div class="container">
        <div class="content">
          <h2 class="title">Fique por dentro das <span class="highlight">Novidades</span></h2>
          <p class="description">
            Receba dicas de Frontend e arquitetura BaaS diretamente no seu e-mail. 
            Sem spam, apenas conteúdo técnico.
          </p>
  
          <form @submit.prevent="handleSubmit" class="newsletter-form">
            <div class="input-group">
              <input 
                v-model="email" 
                type="text" 
                placeholder="Seu melhor e-mail" 
                :class="{ 'input-error': errorMessage }"
              />
              <button type="submit" class="btn-submit">Assinar</button>
            </div>
            
            <p v-if="errorMessage" class="error-text">{{ errorMessage }}</p>
            
            <p v-if="successMessage" class="success-text">{{ successMessage }}</p>
          </form>
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  import { ref, watch } from 'vue';
  
  const email = ref('');
  const errorMessage = ref('');
  const successMessage = ref('');
  
  // O watch "vigia" o que o usuário digita em tempo real
  watch(email, (newValue) => {
    // Se o usuário começar a digitar, limpamos o erro de "campo vazio"
    if (newValue.length > 0) {
      errorMessage.value = '';
    }
    
    // Exemplo de vigia: se ele digitar algo que não parece e-mail após 5 caracteres
    if (newValue.length > 5 && !newValue.includes('@')) {
      errorMessage.value = 'Isso ainda não parece um e-mail válido...';
    } else {
      errorMessage.value = '';
    }
  });
  
  const handleSubmit = () => {
    // Validação ao enviar
    if (!email.value) {
      errorMessage.value = 'O campo de e-mail é obrigatório!';
      return;
    }
  
    const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
    if (!emailRegex.test(email.value)) {
      errorMessage.value = 'Por favor, insira um e-mail real.';
      return;
    }
  
    // Simulação de sucesso
    errorMessage.value = '';
    successMessage.value = '🚀 Inscrito com sucesso! Verifique sua caixa de entrada.';
    email.value = ''; // Limpa o campo
  };
  </script>
  
  <style scoped>
  .newsletter {
    background-color: #0f172a;
    padding: 80px 20px;
    font-family: sans-serif;
    color: white;
    text-align: center;
  }
  
  .container {
    max-width: 600px;
    margin: 0 auto;
  }
  
  .title {
    font-size: 2rem;
    font-weight: 800;
    margin-bottom: 15px;
  }
  
  .highlight {
    color: #60a5fa;
  }
  
  .description {
    color: #94a3b8;
    margin-bottom: 30px;
    line-height: 1.6;
  }
  
  .newsletter-form {
    position: relative;
    width: 100%;
  }
  
  .input-group {
    display: flex;
    gap: 10px;
    background: rgba(30, 41, 59, 0.5);
    padding: 8px;
    border-radius: 12px;
    border: 1px solid #334155;
    transition: border-color 0.3s;
  }
  
  .input-group:focus-within {
    border-color: #60a5fa;
  }
  
  input {
    flex: 1;
    background: transparent;
    border: none;
    outline: none;
    color: white;
    padding: 10px 15px;
    font-size: 1rem;
  }
  
  .input-error {
    border-color: #ef4444 !important;
  }
  
  .btn-submit {
    background-color: #2563eb;
    color: white;
    border: none;
    padding: 12px 25px;
    border-radius: 8px;
    font-weight: bold;
    cursor: pointer;
    transition: background 0.3s;
  }
  
  .btn-submit:hover {
    background-color: #1d4ed8;
  }
  
  /* Estilos de mensagens */
  .error-text {
    color: #ef4444;
    font-size: 0.85rem;
    margin-top: 10px;
    text-align: left;
    padding-left: 10px;
  }
  
  .success-text {
    color: #34d399;
    font-size: 0.95rem;
    margin-top: 15px;
    font-weight: 600;
  }
  
  @media (max-width: 480px) {
    .input-group {
      flex-direction: column;
      background: transparent;
      border: none;
      padding: 0;
    }
    
    input {
      background: rgba(30, 41, 59, 0.5);
      border: 1px solid #334155;
      border-radius: 8px;
      margin-bottom: 10px;
    }
  }
  </style>