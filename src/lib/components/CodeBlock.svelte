<script lang="ts">
  export let code = '';
  let copied = false;

  function copyCode() {
    if (!code) return;
    navigator.clipboard.writeText(code).then(() => {
      copied = true;
      setTimeout(() => (copied = false), 1500);
    });
  }
</script>

<div class="code-container">
  <button class="copy-btn" on:click={copyCode}>
    {#if copied}Copied!{:else}Copy{/if}
  </button>
  <pre><code>{code}</code></pre>
</div>

<style>
.code-container { position: relative; max-width: 100%; }
pre { padding: 1rem; overflow: auto; border-radius: 6px; border: 1px solid #e6f1fa; font-family: 'Fira Mono', monospace; line-height: 1.35; background: #f7fbfe; }
.copy-btn { position: absolute; top: 1rem; right: 0.5rem; background: rgba(0,0,0,0.06); border: 1px solid rgba(0,0,0,0.08); padding: 0.25rem 0.5rem; font-weight: 700; font-size: 0.8rem; border-radius: 4px; cursor: pointer; z-index: 5; }
.copy-btn:active { transform: translateY(1px); }

/* Dark mode */
:global([data-theme='dark']) .code-container pre { background: rgba(10,25,55,0.95); border-color: rgba(255,255,255,0.1); color: rgba(220,230,255,0.95); box-shadow: inset 0 0 6px rgba(0,0,0,0.2); }
:global([data-theme='dark']) .copy-btn { background: rgba(30,60,110,0.7); border-color: rgba(255,255,255,0.25); color: rgba(220,230,255,0.95); }
:global([data-theme='dark']) .copy-btn:hover { background: rgba(40,90,160,0.85); }
</style>
