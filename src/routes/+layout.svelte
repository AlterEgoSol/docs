<script lang="ts">
  import { page } from '$app/stores';
  import '../app.css';
</script>

<div class="layout">
  <header>
    <div class="logo">
      <a href="/">AlterEgo</a>
    </div>
    <nav class="top-nav">
      <a href="/features">Features</a>
      <a href="/how-it-works">How It Works</a>
      <a href="/faq">FAQ</a>
      <a href="https://alterego.app/join-waitlist" class="join-waitlist">Join Waitlist</a>
    </nav>
  </header>

  <div class="content">
    <nav class="sidebar">
      <div class="nav-group">
        <div class="nav-header">Getting Started</div>
        <a href="/docs/getting-started" class:active={$page.url.pathname === '/docs/getting-started'}>Getting Started</a>
        <a href="/docs/creating-your-alterego" class:active={$page.url.pathname === '/docs/creating-your-alterego'}>Creating Your AlterEgo</a>
      </div>
      
      <div class="nav-group">
        <div class="nav-header">Configuration</div>
        <a href="/docs/behavior-training" class:active={$page.url.pathname === '/docs/behavior-training'}>Behavior Training</a>
        <a href="/docs/permissions" class:active={$page.url.pathname === '/docs/permissions'}>Permissions</a>
        <a href="/docs/monetization" class:active={$page.url.pathname === '/docs/monetization'}>Monetization Settings</a>
      </div>

      <div class="nav-group">
        <div class="nav-header">Advanced Features</div>
        <a href="/docs/marketplace" class:active={$page.url.pathname === '/docs/marketplace'}>Decentralized Marketplace</a>
        <a href="/docs/legacy-mode" class:active={$page.url.pathname === '/docs/legacy-mode'}>Legacy Mode</a>
        <a href="/docs/cross-chain" class:active={$page.url.pathname === '/docs/cross-chain'}>Cross-Chain Integration</a>
      </div>

      <div class="nav-group">
        <div class="nav-header">Resources</div>
        <a href="/docs/faq" class:active={$page.url.pathname === '/docs/faq'}>FAQs</a>
      </div>
    </nav>

    <main>
      <slot />
    </main>
  </div>
</div>

<style>
  .layout {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
  }

  header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 2rem;
    border-bottom: 1px solid #eaeaea;
  }

  .logo a {
    font-size: 1.5rem;
    font-weight: bold;
    color: #0066cc;
    text-decoration: none;
  }

  .top-nav {
    display: flex;
    gap: 2rem;
    align-items: center;
  }

  .top-nav a {
    text-decoration: none;
    color: #333;
  }

  .join-waitlist {
    background-color: #0066cc;
    color: white !important;
    padding: 0.5rem 1rem;
    border-radius: 4px;
  }

  .content {
    display: flex;
    flex: 1;
  }

  .sidebar {
    width: 280px;
    padding: 2rem;
    border-right: 1px solid #eaeaea;
    background: #f8f9fa;
    height: calc(100vh - 64px);
    position: sticky;
    top: 0;
    overflow-y: auto;
  }

  .nav-group {
    margin-bottom: 2rem;
  }

  .nav-header {
    font-weight: 600;
    color: #666;
    margin-bottom: 0.5rem;
    font-size: 0.875rem;
    text-transform: uppercase;
  }

  .sidebar a {
    display: block;
    padding: 0.5rem 0;
    color: #333;
    text-decoration: none;
    font-size: 0.9rem;
  }

  .sidebar a:hover {
    color: #0066cc;
  }

  .sidebar a.active {
    color: #0066cc;
    font-weight: 500;
  }

  main {
    flex: 1;
    padding: 2rem;
    max-width: 900px;
  }
</style> 