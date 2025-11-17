<script lang="ts">
	import Installation from '$lib/docs/Installation.svx';
</script>

<section class="Installation">
	<h2>Installation</h2>
	<p>To install the package, run the following command in your terminal:</p>
		<Installation />
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
		margin: 1.25rem 0;
		padding: 1rem;
		border: 1px solid #b6cfe4;
		border-radius: 8px;
		background-color: #e3f2ff;
	}

/* Dark Mode */
:global([data-theme='dark']) {.Installation, .System-Overview, .Tools-and-Features {
  background-color: rgba(20, 40, 75, 0.85); /* deep navy */
  border-color: rgba(255, 255, 255, 0.15);
  color: rgba(235, 240, 255, 0.9);
  box-shadow: none;
  transition: background-color 0.3s ease, color 0.3s ease, box-shadow 0.3s ease;
}}

/* Hover */
:global([data-theme='dark']) {.Installation:hover, .System-Overview:hover, .Tools-and-Features:hover {
  box-shadow: 0 4px 12px rgba(255, 255, 255, 0.3); /* subtle glow on hover */
}}

/* Headings and text */
:global([data-theme='dark']) h2 {
  color: #cce0ff; /* soft blue */
}

:global([data-theme='dark']) p {
  color: rgba(220, 230, 255, 0.85); /* readable soft white-blue */
}

/* Markdown / code boxes inside sections */
:global([data-theme='dark']) {.Installation pre, .System-Overview pre, .Tools-and-Features pre {
  background-color: rgba(60, 85, 130, 0.9); /* noticeably lighter than section bg */
  border: 1px solid rgba(255, 255, 255, 0.15);
  border-radius: 6px;
  padding: 0.75rem;
  color: #e0f0ff; /* brighter text for readability */
  overflow-x: auto;
  box-shadow: 0 2px 10px rgba(0,0,0,0.4);
  transition: background-color 0.3s ease, color 0.3s ease;
}}
</style>