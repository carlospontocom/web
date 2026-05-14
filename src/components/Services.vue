<template>
    <section class="services">
      <div class="container">
        <div class="header">
          <h2 class="section-title">Nossas <span class="gradient-text">Especialidades</span></h2>
          <p class="section-subtitle">Soluções completas para levar sua ideia do protótipo à produção.</p>
        </div>
  
        <div class="services-grid">
          <div class="card">
            <div class="icon">🎨</div>
            <h3 class="card-title">Frontend</h3>
            <p class="card-text">
              Interfaces modernas e responsivas com <strong>Vue.js</strong> e React. Foco total em UX/UI e performance.
            </p>
          </div>
  
          <div class="card">
            <div class="icon">🚀</div>
            <h3 class="card-title">NodeJS</h3>
            <p class="card-text">
              APIs robustas e escaláveis. Construção de microsserviços e integração de sistemas com alta eficiência.
            </p>
          </div>
  
          <div class="card">
            <div class="icon">🔥</div>
            <h3 class="card-title">Firebase</h3>
            <p class="card-text">
              Backend as a Service para agilizar o deploy. Autenticação, Real-time Database e Hosting seguro.
            </p>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <style scoped>
  .services {
    background-color: #0f172a; /* Mesmo fundo do Hero */
    padding: 100px 20px;
    font-family: sans-serif;
    color: white;
  }
  
  .container {
    max-width: 1200px;
    margin: 0 auto;
  }
  
  .header {
    text-align: center;
    margin-bottom: 60px;
  }
  
  .section-title {
    font-size: 2.5rem;
    font-weight: 800;
    margin-bottom: 15px;
  }
  
  .gradient-text {
    background: linear-gradient(90deg, #60a5fa, #34d399);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }
  
  .section-subtitle {
    color: #94a3b8;
    font-size: 1.1rem;
  }
  
  /* Grid de Cards */
  .services-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 30px;
  }
  
  /* Estilo do Card */
  .card {
    background: rgba(30, 41, 59, 0.5);
    border: 1px solid #334155;
    padding: 40px;
    border-radius: 16px;
    transition: all 0.3s ease;
    cursor: default;
  }
  
  .card:hover {
    transform: translateY(-10px);
    border-color: #60a5fa;
    background: rgba(30, 41, 59, 0.8);
    box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.2);
  }
  
  .icon {
    font-size: 2.5rem;
    margin-bottom: 20px;
  }
  
  .card-title {
    font-size: 1.5rem;
    font-weight: 700;
    margin-bottom: 15px;
    color: #f8fafc;
  }
  
  .card-text {
    color: #94a3b8;
    line-height: 1.6;
  }
  
  /* Responsividade extra */
  @media (max-width: 768px) {
    .section-title {
      font-size: 2rem;
    }
  }
  </style>