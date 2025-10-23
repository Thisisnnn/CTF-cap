<script>
function copyCode(event) {
  const button = /** @type {HTMLElement} */ (event.currentTarget);
  const wrapper = button.closest('.code-wrapper');
  const code = wrapper?.querySelector('pre code')?.innerText ?? '';
  if (!code) return;

  navigator.clipboard.writeText(code).then(() => {
    const original = button.textContent;
    button.textContent = 'Copied!';
    setTimeout(() => (button.textContent = original ?? 'Copy'), 1500);
  }).catch(() => {
    button.textContent = 'Failed';
    setTimeout(() => (button.textContent = 'Copy'), 1500);
  });
}
</script>

<section class="Installation">
	<h2>Installation</h2>
	<p>To install the package, run the following command in your terminal:</p>
	<div class="code-wrapper">
		<button class="copy-btn" on:click={copyCode}>Copy</button>
		<pre><code>git clone
python3 installation.py
</code></pre>
	</div>
</section>

<section class="System-Overview">
	<h2>System Overview</h2>
	<p>This section provides an overview of the system architecture and its main components. It covers the core functionalities, design principles, and how different modules interact with each other to deliver a seamless user experience.</p>
</section>

<section class="Tools-and-Features">
	<h2>Tools and Features</h2>
	<p>CTFcap comes with a variety of tools and features designed to enhance your CTF experience.</p>
</section>

<style>
	.Installation, .System-Overview, .Tools-and-Features {
		margin: 2rem 0;
		padding: 1rem;
		border: 1px solid #b6cfe4;
		border-radius: 8px;
		background-color: #e3f2ff;
	}

	.code-wrapper {
		position: relative;
		display: block;
		max-width: 100%;
	}
	.code-wrapper pre {
		padding: 1rem; 
		overflow: auto;
		background: #f7fbfe;
		border-radius: 6px;
		border: 1px solid #e6f1fa;
		margin: 0;
		line-height: 1.35;
	}
	.copy-btn {
		position: absolute;
		top: 1rem; 
		right: 0.5rem;
		background: rgba(0,0,0,0.06);
		border: 1px solid rgba(0,0,0,0.08);
		padding: 0.25rem 0.5rem;
		font-weight: 700;
		font-size: 0.8rem;
		border-radius: 4px;
		cursor: pointer;
		z-index: 5;
	}
	.copy-btn:active { transform: translateY(1px); }
</style>