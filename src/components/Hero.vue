<template> 
<section class="hero">
    <div class="bg-blur blur-1"></div>
    <div class="bg-blur blur-2"></div>

    <div class="container">
      <div class="content-wrapper">
        
        <div class="text-content">
          <h1 class="title">
            Frontend Poderoso, <br />
            <span class="gradient-text">Sem Medo do Backend.</span>
          </h1>
          <p class="description">
            Domine a arte de criar interfaces incríveis enquanto o 
            <strong>BaaS</strong> cuida da infraestrutura. 
            Autenticação e banco de dados prontos para escalar.
          </p>
          
          <div class="actions">
            <button class="btn btn-primary">Começar Agora</button>
            <button class="btn btn-secondary">Ver Documentação</button>
          </div>
        </div>

        <div class="code-box">
          <div class="window-controls">
            <span class="dot red"></span>
            <span class="dot yellow"></span>
            <span class="dot green"></span>
          </div>
          <pre><code><span class="keyword">import</span> { createClient } <span class="keyword">from</span> <span class="string">'@baas/sdk'</span>

<span class="comment">// O Frontend no controle</span>
<span class="keyword">const</span> user = <span class="keyword">await</span> baas.auth.<span class="function">signIn</span>({
  email: <span class="string">'dev@frontend.com'</span>,
  password: <span class="string">'********'</span>
})</code></pre>
        </div>

      </div>
    </div>
  </section>
</template>

<style scoped>
/* Reset básico e variáveis */
.hero {
    --primary-color: #2563eb;
    --bg-dark: #0f172a;
    --text-slate: #94a3b8;

    position: relative;
    background-color: var(--bg-dark);
    color: white;
    padding: 80px 20px;
    overflow: hidden;
    font-family: sans-serif;
}

.container {
    max-width: 1200px;
    margin: 0 auto;
    position: relative;
    z-index: 10;
}

.content-wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 50px;
}

@media (min-width: 768px) {
    .content-wrapper {
        flex-direction: row;
        text-align: left;
    }
}

/* Tipografia */
.title {
    font-size: 2.5rem;
    font-weight: 800;
    line-height: 1.2;
    margin-bottom: 24px;
}

.gradient-text {
    background: linear-gradient(90deg, #60a5fa, #34d399);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.description {
    font-size: 1.2rem;
    color: var(--text-slate);
    margin-bottom: 32px;
    max-width: 600px;
}

/* Botões */
.actions {
    display: flex;
    gap: 16px;
}

.btn {
    padding: 12px 24px;
    border-radius: 8px;
    font-weight: bold;
    cursor: pointer;
    transition: transform 0.2s;
    border: none;
}

.btn:hover {
    transform: scale(1.05);
}

.btn-primary {
    background-color: var(--primary-color);
    color: white;
}

.btn-secondary {
    background-color: transparent;
    border: 1px solid #334155;
    color: white;
}

/* Editor de Código */
.code-box {
    background: rgba(30, 41, 59, 0.7);
    backdrop-filter: blur(8px);
    border: 1px solid #334155;
    border-radius: 12px;
    padding: 20px;
    width: 100%;
    max-width: 500px;
    box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.3);
}

.window-controls {
    display: flex;
    gap: 8px;
    margin-bottom: 15px;
}

.dot {
    width: 12px;
    height: 12px;
    border-radius: 50%;
}

.red {
    background: #ef4444;
}

.yellow {
    background: #f59e0b;
}

.green {
    background: #10b981;
}

pre {
    margin: 0;
    font-family: monospace;
    color: #93c5fd;
    line-height: 1.5;
}

/* Syntax Highlighting */
.keyword {
    color: #c084fc;
}

.string {
    color: #34d399;
}

.comment {
    color: #64748b;
}

.function {
    color: #60a5fa;
}

/* Background Blurs */
.bg-blur {
    position: absolute;
    width: 400px;
    height: 400px;
    border-radius: 50%;
    filter: blur(100px);
    opacity: 0.15;
    pointer-events: none;
}

.blur-1 {
    top: -100px;
    left: -100px;
    background: #2563eb;
}

.blur-2 {
    bottom: -100px;
    right: -100px;
    background: #9333ea;
}
</style>