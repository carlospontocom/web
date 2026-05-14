<template>
    <section class="firebase-services">
      <div class="container">
        <div class="content-wrapper">
          
          <div class="image-column">
            <div class="image-wrapper">
              <img src="https://firebase.google.com/static/images/brand-guidelines/logo-vertical.png" alt="Firebase Logo" class="main-image" />
              <div class="image-decoration"></div>
            </div>
          </div>
  
          <div class="text-column">
            <h2 class="title">Potencialize seu App com <span class="highlight">Firebase</span></h2>
            <p class="description">
              O Firebase é a plataforma do Google que oferece toda a infraestrutura necessária para o seu frontend, permitindo que você foque na experiência do usuário.
            </p>
  
            <ul class="features-list">
              <li>
                <span class="icon">🔐</span>
                <div>
                  <strong class="feature-title">Autenticação Simplificada</strong>
                  <p>Login com Google, Facebook, E-mail e mais, configurado em minutos.</p>
                </div>
              </li>
              <li>
                <span class="icon">📊</span>
                <div>
                  <strong class="feature-title">Cloud Firestore</strong>
                  <p>Banco de dados NoSQL em tempo real, escalável e extremamente rápido.</p>
                </div>
              </li>
              <li>
                <span class="icon">☁️</span>
                <div>
                  <strong class="feature-title">Cloud Storage & Hosting</strong>
                  <p>Armazenamento de arquivos e hospedagem global com SSL automático.</p>
                </div>
              </li>
            </ul>
          </div>
  
        </div>
      </div>
    </section>
  </template>
  
  <style scoped>
  .firebase-services {
    background-color: #0f172a;
    padding: 100px 20px;
    color: white;
    font-family: sans-serif;
  }
  
  .container {
    max-width: 1200px;
    margin: 0 auto;
  }
  
  .content-wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 60px;
  }
  
  @media (min-width: 992px) {
    .content-wrapper {
      flex-direction: row; /* Duas colunas no desktop */
      text-align: left;
    }
  }
  
  /* Coluna da Imagem */
  .image-column {
    flex: 1;
    display: flex;
    justify-content: center;
    position: relative;
  }
  
  .image-wrapper {
    position: relative;
    z-index: 2;
    background: rgba(30, 41, 59, 0.3);
    padding: 40px;
    border-radius: 24px;
    border: 1px solid rgba(255, 255, 255, 0.1);
    backdrop-filter: blur(10px);
  }
  
  .main-image {
    max-width: 250px;
    height: auto;
    filter: drop-shadow(0 0 20px rgba(255, 166, 17, 0.4));
  }
  
  .image-decoration {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 300px;
    height: 300px;
    background: radial-gradient(circle, rgba(255, 166, 17, 0.2) 0%, transparent 70%);
    z-index: -1;
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
    color: #ffa611; /* Cor oficial do Firebase */
  }
  
  .description {
    color: #94a3b8;
    font-size: 1.1rem;
    line-height: 1.6;
    margin-bottom: 40px;
  }
  
  /* Lista de Funcionalidades */
  .features-list {
    list-style: none;
    padding: 0;
    display: flex;
    flex-direction: column;
    gap: 30px;
  }
  
  .features-list li {
    display: flex;
    gap: 20px;
    align-items: flex-start;
  }
  
  .icon {
    font-size: 1.5rem;
    background: rgba(255, 166, 17, 0.1);
    padding: 10px;
    border-radius: 12px;
    line-height: 1;
  }
  
  .feature-title {
    display: block;
    font-size: 1.2rem;
    margin-bottom: 5px;
    color: #f8fafc;
  }
  
  .features-list p {
    color: #94a3b8;
    margin: 0;
    font-size: 0.95rem;
  }
  
  @media (max-width: 768px) {
    .title {
      font-size: 2rem;
    }
  }
  </style>