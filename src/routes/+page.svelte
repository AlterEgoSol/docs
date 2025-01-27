<script>
  import { base } from '$app/paths';
</script>

<div class="hero">
  <h1>Create Your Digital Twin<br />on the Solana Blockchain</h1>
  <p class="hero-subtitle">Train, deploy, and monetize your AI clone. Let it handle tasks while you focus on what matters most.</p>
  <div class="hero-buttons">
    <a href="https://alterego.app/try-demo" class="button primary">Try Demo</a>
    <a href="/docs/getting-started" class="button secondary">Documentation</a>
  </div>
</div>

<div class="features">
  <h2>Features</h2>
  <div class="feature-grid">
    <div class="feature-card">
      <h3>Behavioral Training</h3>
      <p>Train your AI clone with your communication style, decision-making patterns, and preferences.</p>
    </div>
    <div class="feature-card">
      <h3>Smart Contracts</h3>
      <p>Secure your AI clone's operations with tamper-proof smart contracts on Solana.</p>
    </div>
    <div class="feature-card">
      <h3>Monetization</h3>
      <p>Earn passive income by letting your AI clone work in the decentralized marketplace.</p>
    </div>
  </div>
</div>

<style>
  .hero {
    text-align: center;
    padding: 4rem 2rem;
    background: linear-gradient(to bottom, #f8f9fa, #ffffff);
  }

  .hero h1 {
    font-size: 3rem;
    line-height: 1.2;
    margin-bottom: 1rem;
  }

  .hero-subtitle {
    font-size: 1.25rem;
    color: #666;
    max-width: 600px;
    margin: 0 auto 2rem;
  }

  .hero-buttons {
    display: flex;
    gap: 1rem;
    justify-content: center;
  }

  .button {
    padding: 0.75rem 1.5rem;
    border-radius: 4px;
    font-weight: 500;
    transition: all 0.2s;
  }

  .button.primary {
    background: var(--primary-color);
    color: white;
  }

  .button.secondary {
    background: white;
    color: var(--primary-color);
    border: 1px solid var(--primary-color);
  }

  .button:hover {
    text-decoration: none;
    transform: translateY(-1px);
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  }

  .features {
    padding: 4rem 2rem;
  }

  .features h2 {
    text-align: center;
    margin-bottom: 3rem;
  }

  .feature-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 2rem;
    max-width: 1200px;
    margin: 0 auto;
  }

  .feature-card {
    background: white;
    padding: 2rem;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  }

  .feature-card h3 {
    color: var(--primary-color);
    margin-bottom: 1rem;
  }

  @media (max-width: 768px) {
    .hero h1 {
      font-size: 2rem;
    }

    .hero-subtitle {
      font-size: 1.1rem;
    }

    .feature-grid {
      grid-template-columns: 1fr;
    }
  }
</style>
