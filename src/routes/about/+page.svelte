<section class="about-page">
  <h1>About CTFcap</h1>
  <p class="subtitle">An advanced capture-the-flag platform built for security enthusiasts</p>

  <div class="section mission">
    <h2>Our Mission</h2>
    <p>CTFcap is designed to revolutionize how security professionals and enthusiasts practice their skills. We provide a robust platform for hosting, participating in, and learning from capture-the-flag challenges.</p>
  </div>

  <div class="section features">
    <h2>Key Features</h2>
    <ul class="feature-list">
      <li>Tools made for CTF competitions</li>
    </ul>
  </div>

  <div class="section team">
    <h2>Our Team</h2>
    <div class="team-grid">
      <div class="team-member">
        <h3>Alice Smith</h3>
        <p>Security Research Lead</p>
        <span class="tag">Exploit Dev</span>
      </div>
      <div class="team-member">
        <h3>Bob Johnson</h3>
        <p>Platform Architect</p>
        <span class="tag">Infrastructure</span>
      </div>
      <div class="team-member">
        <h3>Carol Davis</h3>
        <p>Community Lead</p>
        <span class="tag">Education</span>
      </div>
    </div>
  </div>

  <div class="section tech">
    <h2>Technology Stack</h2>
    <div class="tech-stack">
      <span class="tech-item">SvelteKit</span>
      <span class="tech-item">Python</span>
    </div>
  </div>
</section>

<style>
  :root {
    --primary: #2563eb;
    --secondary: #3b82f6;
    --bg: #ffffff;
    --text: #0f172a;
    --muted: #64748b;
  }

  .about-page {
    max-width: 900px;
    margin: 0 auto;
    padding: 2rem;
    color: var(--text);
  }

  h1 {
    font-size: 2.5rem;
    text-align: center;
    margin-bottom: 0.5rem;
    background: linear-gradient(135deg, var(--primary), var(--secondary));
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }

  .subtitle {
    text-align: center;
    color: var(--muted);
    margin-bottom: 3rem;
    font-size: 1.1rem;
  }

  .section {
    background: white;
    border-radius: 12px;
    padding: 1.5rem;
    margin-bottom: 2rem;
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
    border: 1px solid #e5e7eb;
  }

  .section h2 {
    font-size: 1.4rem;
    margin-bottom: 1rem;
    color: var(--text);
  }

  .feature-list {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 1rem;
    list-style: none;
    padding: 0;
  }

  .feature-list li {
    padding: 0.5rem;
    background: #f8fafc;
    border-radius: 6px;
    border: 1px solid #e5e7eb;
  }

  .team-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 2rem;
    margin-top: 1.5rem;
  }

  .team-member {
    text-align: center;
    padding: 1.5rem;
    background: #f8fafc;
    border-radius: 8px;
    border: 1px solid #e5e7eb;
  }

  .team-member h3 {
    margin: 0;
    font-size: 1.2rem;
    color: var(--text);
  }

  .team-member p {
    color: var(--muted);
    margin: 0.3rem 0;
  }

  .tag {
    display: inline-block;
    padding: 0.2rem 0.6rem;
    background: var(--primary);
    color: white;
    border-radius: 999px;
    font-size: 0.8rem;
  }

  .tech-stack {
    display: flex;
    flex-wrap: wrap;
    gap: 0.8rem;
  }

  .tech-item {
    padding: 0.4rem 0.8rem;
    background: #f1f5f9;
    border-radius: 6px;
    font-size: 0.9rem;
    color: var(--text);
    border: 1px solid #e5e7eb;
  }

  /* Add dark mode styles */
  :global([data-theme='dark']) .section {
    background: rgba(13, 75, 130, 0.2);
    border-color: rgba(255, 255, 255, 0.1);
    box-shadow: 0 4px 6px rgb(255, 255, 255);
  }

  :global([data-theme='dark']) .feature-list li,
  :global([data-theme='dark']) .team-member,
  :global([data-theme='dark']) .tech-item {
    background: rgba(13, 75, 130, 0.3);
    border-color: rgba(255, 255, 255, 0.1);
  }

  :global([data-theme='dark']) .tag {
    background: var(--primary);
  }

  :global([data-theme='dark']) .team-member h3,
  :global([data-theme='dark']) .section h2, 
  :global([data-theme='dark']) .feature-list li, 
  :global([data-theme='dark']) .tech-item {
    color: rgba(255, 255, 255, 0.85);
  }

  :global([data-theme='dark']) p,
  :global([data-theme='dark']) .subtitle {
    color: rgba(255, 255, 255, 0.6);
  }

  @media (max-width: 640px) {
    .about-page {
      padding: 1rem;
    }
    
    .team-grid {
      grid-template-columns: 1fr;
      gap: 1.5rem;
    }
  }
</style>
