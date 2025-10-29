<section class="blog">
  <h1>Project Blog</h1>
  <p>Follow our journey as we build our open-source operating system from scratch.</p>

  <article class="blog-post">
    <h2>Welcome to the Project</h2>
    <small>September 2025</small>
    <p>We've just started working on our OS. Our OS is supposed to be made for CTF competition to have all the tools you need.</p>
  </article>

  <article class="blog-post">
    <h2>Laying the Foundations: LFS</h2>
    <small>October 2025</small>
    <p>Trying to automatize LFS installation with Python3</p>
  </article>
</section>

<style>
  /* LIGHT MODE */
  :root {
    --card-bg: #ffffff;
    --card-border: #e6edf3;
    --accent: #2563eb;
    --muted: #6b7280;
    --text: #0f1724;
  }

  .blog{
    max-width: 700px;
    margin: 0 auto;
    font-family: system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    padding: 2rem;
    color: var(--text);
    display: grid;
    gap: 1.6rem;
  }

  .blog-post{
    background: var(--card-bg);
    border: 1px solid var(--card-border);
    border-radius: 10px;
    padding: 1rem 1.25rem;
    margin-bottom: 0;
    box-shadow: 0 4px 10px rgba(16,24,40,0.04);
    transition: box-shadow 160ms ease, transform 160ms ease;
    will-change: transform;
    position: relative;
    z-index: 1;
    transform-origin: center top;
  }

  .blog-post:hover{
    box-shadow: 0 12px 32px rgba(16,24,40,0.08);
    transform: translateY(-6px) scale(1.02);
    z-index: 3;
  }

  .blog-post h2{
    margin: 0 0 0.35rem 0;
    font-size: 1.25rem;
    color: var(--text);
  }
  .blog-post small{
    color: var(--muted);
    display: inline-block;
    margin-bottom: 0.5rem;
    font-size: 0.85rem;
  }

  .blog-post p{
    margin: 0.5rem 0 0.9rem 0;
    line-height: 1.5;
    color: rgba(15,23,36,0.9);
  }

  /* DARK MODE */
  :global([data-theme='dark']) .blog{
    color: rgba(235, 240, 255, 0.9);
  }

  :global([data-theme='dark']) .blog-post {
    background: rgba(20, 40, 75, 0.85); /* deep navy */
    border-color: rgba(255, 255, 255, 0.15);
    box-shadow: 0 4px 10px rgba(255, 255, 255, 0.25);
  }

  :global([data-theme='dark']) .blog-post:hover {
    box-shadow: 0 12px 32px rgba(0, 0, 0, 0.3);
    transform: translateY(-6px) scale(1.02);
  }

  :global([data-theme='dark']) .blog-post h2{
    color: rgba(235, 240, 255, 0.95);
  }

  :global([data-theme='dark']) .blog-post small {
    color: rgba(180, 200, 255, 0.7);
  }

  :global([data-theme='dark']) .blog-post p {
    color: rgba(235, 240, 255, 0.85);
  }

  @media (max-width: 560px){
    .blog{
      padding: 1rem;
      gap: 1.1rem;
    }
    .blog-post{
      padding: 0.9rem 1rem;
    }
  }
</style>
