<template>
    <section class="data-management">
      <div class="container">
        <div class="content-wrapper">
          
          <div class="text-column">
            <h2 class="title">Sistemas de <span class="highlight">Chat & Dados</span> em Tempo Real</h2>
            <p class="description">
              Crie experiências interativas onde os dados fluem instantaneamente entre os usuários, sem a necessidade de atualizar a página.
            </p>
  
            <div class="features-grid">
              <div class="feature-item">
                <div class="feature-icon">💬</div>
                <div class="feature-info">
                  <strong class="feature-label">Chat em Tempo Real</strong>
                  <p>Mensageria instantânea com WebSockets integrados nativamente pelo BaaS.</p>
                </div>
              </div>
  
              <div class="feature-item">
                <div class="feature-icon">📂</div>
                <div class="feature-info">
                  <strong class="feature-label">Gerenciador de Dados</strong>
                  <p>Painéis administrativos para criar, ler, editar e excluir informações com facilidade.</p>
                </div>
              </div>
            </div>
          </div>
  
          <div class="image-column">
            <div class="image-wrapper">
              <div class="chat-mockup">
                <div class="chat-header">Admin Dashboard</div>
                <div class="chat-message">Novo usuário conectado...</div>
                <div class="chat-message user">Dados sincronizados! ✅</div>
                <div class="chat-input"></div>
              </div>
              <div class="image-decoration"></div>
            </div>
          </div>
  
        </div>
      </div>
    </section>
  </template>
  
  <style scoped>
  .data-management {
    background-color: #0f172a; /* Mantém a cor para continuidade */
    padding: 100px 20px;
    color: white;
    font-family: sans-serif;
    border-top: 1px solid rgba(255, 255, 255, 0.05);
  }
  
  .container {
    max-width: 1200px;
    margin: 0 auto;
  }
  
  .content-wrapper {
    display: flex;
    flex-direction: column-reverse; /* No mobile, o texto continua em cima */
    align-items: center;
    gap: 60px;
  }
  
  @media (min-width: 992px) {
    .content-wrapper {
      flex-direction: row; /* No desktop, alinha lado a lado */
      text-align: left;
    }
  }
  
  /* Coluna de Texto */
  .text-column {
    flex: 1;
  }
  
  .title {
    font-size: 2.5rem;
    font-weight: 800;
    margin-bottom: 20px;
    line-height: 1.2;
  }
  
  .highlight {
    color: #34d399; /* Verde para diferenciar do laranja do Firebase */
  }
  
  .description {
    color: #94a3b8;
    font-size: 1.1rem;
    line-height: 1.6;
    margin-bottom: 40px;
  }
  
  .features-grid {
    display: flex;
    flex-direction: column;
    gap: 25px;
  }
  
  .feature-item {
    display: flex;
    gap: 15px;
    background: rgba(255, 255, 255, 0.03);
    padding: 20px;
    border-radius: 12px;
    border: 1px solid rgba(255, 255, 255, 0.05);
  }
  
  .feature-icon {
    font-size: 1.5rem;
  }
  
  .feature-label {
    display: block;
    font-size: 1.1rem;
    color: #f8fafc;
    margin-bottom: 4px;
  }
  
  .feature-info p {
    margin: 0;
    color: #94a3b8;
    font-size: 0.9rem;
  }
  
  /* Coluna da Imagem (Lado Direito) */
  .image-column {
    flex: 1;
    display: flex;
    justify-content: center;
    position: relative;
  }
  
  .image-wrapper {
    position: relative;
    z-index: 2;
  }
  
  .chat-mockup {
    width: 300px;
    background: #1e293b;
    border-radius: 20px;
    padding: 20px;
    border: 4px solid #334155;
    box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.5);
  }
  
  .chat-header {
    height: 20px;
    background: #334155;
    border-radius: 10px;
    margin-bottom: 20px;
    font-size: 10px;
    text-align: center;
    line-height: 20px;
    color: #94a3b8;
  }
  
  .chat-message {
    background: #334155;
    padding: 10px;
    border-radius: 8px;
    margin-bottom: 10px;
    font-size: 12px;
    width: 80%;
  }
  
  .chat-message.user {
    background: #059669;
    margin-left: 20%;
    text-align: right;
  }
  
  .chat-input {
    height: 30px;
    background: #0f172a;
    border-radius: 15px;
    margin-top: 30px;
  }
  
  .image-decoration {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 350px;
    height: 350px;
    background: radial-gradient(circle, rgba(52, 211, 153, 0.15) 0%, transparent 70%);
    z-index: -1;
  }
  
  @media (max-width: 768px) {
    .title {
      font-size: 2rem;
    }
  }
  </style>