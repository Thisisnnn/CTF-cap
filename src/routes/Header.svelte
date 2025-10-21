<script lang="ts">
	import { page } from '$app/state';
	import logo from '$lib/images/svelte-logo.svg';
	import github from '$lib/images/github.svg';
	import {
		Dropdown,
		DropdownItem,
		DropdownMenu,
		DropdownToggle
	} from '@sveltestrap/sveltestrap';
	import 'bootstrap/dist/css/bootstrap.min.css';
</script>

<header>
	<div class="corner">
		<a href="https://svelte.dev/docs/kit">
			<img src={logo} alt="SvelteKit" />
		</a>
	</div>

	<nav>
		<svg viewBox="0 0 2 3" aria-hidden="true">
			<path d="M0,0 L1,2 C1.5,3 1.5,3 2,3 L2,0 Z" />
		</svg>
		<ul>
			<li aria-current={page.url.pathname === '/' ? 'page' : undefined}>
				<a href="/">Home</a>
			</li>
			<li aria-current={page.url.pathname.startsWith('/docs') ? 'page' : undefined}>
				<a href="/docs">Documentation</a>
			</li>
			<li aria-current={page.url.pathname.startsWith('/blog') ? 'page' : undefined}>
				<a href="/blog">Blog</a>
			</li>
			<Dropdown direction="down">
			<DropdownToggle tag="a" caret class="nav-link">Community</DropdownToggle>
			<DropdownMenu>
				<DropdownItem>Community Support</DropdownItem>
				<DropdownItem>Discord</DropdownItem>
				<DropdownItem>idk</DropdownItem>
			</DropdownMenu>
			</Dropdown>
			<li aria-current={page.url.pathname.startsWith('/dev') ? 'page' : undefined}>
				<a href="/dev">Development</a>
			</li>
			<li aria-current={page.url.pathname === '/about' ? 'page' : undefined}>
				<a href="/about">About</a>
			</li>
		</ul>
		<svg viewBox="0 0 2 3" aria-hidden="true">
			<path d="M0,0 L0,3 C0.5,3 0.5,3 1,2 L2,0 Z" />
		</svg>
	</nav>

	<div class="corner">
		<a href="https://github.com/sveltejs/kit">
			<img src={github} alt="GitHub" />
		</a>
	</div>
</header>

<style>
	header {
		display: flex;
		justify-content: space-between;
	}

	.corner {
		width: 3em;
		height: 3em;
	}

	.corner a {
		display: flex;
		align-items: center;
		justify-content: center;
		width: 100%;
		height: 100%;
	}

	.corner img {
		width: 2em;
		height: 2em;
		object-fit: contain;
	}

	nav {
		display: flex;
		justify-content: center;
		--background: rgba(255, 255, 255, 0.7);
	}

	svg {
		width: 2em;
		height: 3em;
		display: block;
	}

	path {
		fill: var(--background);
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
		background: var(--background);
		background-size: contain;
	}

	li {
		position: relative;
		height: 100%;
	}

	li[aria-current='page']::before {
		--size: 6px;
		content: '';
		width: 0;
		height: 0;
		position: absolute;
		top: 0;
		left: calc(50% - var(--size));
		border: var(--size) solid transparent;
		border-top: var(--size) solid var(--color-theme-1);
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 0.5rem;
		color: var(--color-text);
		font-weight: 700;
		font-size: 0.8rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		color: var(--color-theme-1);
	}

	.nav-link {
  background: transparent !important;
  border: none !important;
  padding: 0 0.5rem;
  font-weight: 700;
  font-size: 0.8rem;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  color: var(--color-text);
  cursor: pointer;
  display: flex;
  align-items: center;
  text-decoration: none; /* removes underline */
}

.nav-link:hover,
.nav-link:focus,
.nav-link:active {
  background: transparent !important;
  color: var(--color-theme-1);
  outline: none;
}

/* align the caret nicely */
.nav-link .dropdown-toggle::after {
  margin-left: 0.25rem;
  vertical-align: middle;
}

.dropdown-menu {
  border: none;            /* remove border */
  box-shadow: none;        /* remove shadow */
  background: white;       /* or match your navbar if you want inline style */
  padding: 0.25rem 0;
}

/* Update dropdown styles */
:global(.dropdown-toggle),
:global(.dropdown-item) {
        font-weight: 700 !important;
        font-size: 0.8rem !important;
        text-transform: uppercase !important;
        letter-spacing: 0.1em !important;
        color: var(--color-text) !important;
        background-color: transparent !important;
        padding: 0.5rem 1rem !important;
        line-height: 1.5 !important;
    }

    :global(.dropdown-menu) {
        background-color: var(--background) !important;
        border: 1px solid rgba(0,0,0,.15) !important;
        border-radius: 6px !important;
        margin-top: 0.5rem !important;
        padding: 0.5rem 0 !important;
        box-shadow: 0 2px 5px rgba(0,0,0,0.1) !important;
    }

    :global(.dropdown-item:hover),
    :global(.dropdown-toggle:hover) {
        color: var(--color-theme-1) !important;
        background-color: transparent !important;
    }

    :global(.dropdown-item:active),
    :global(.dropdown-item:focus),
    :global(.dropdown-item.active) {
        background-color: transparent !important;
        color: var(--color-text) !important;
    }

    /* Remove dropdown arrow spacing */
    :global(.dropdown-toggle::after) {
        margin-left: 0.5em !important;
    }

    :global(.dropdown-item),
    :global(.dropdown-item:active),
    :global(.dropdown-item:focus),
    :global(.dropdown-item.active),
    :global(.dropdown-item:active) {
        background-color: transparent !important;
        transition: none !important;
        color: var(--color-text) !important;
    }

    :global(.dropdown-item:hover) {
        background-color: rgba(0, 0, 0, 0.05) !important;
        color: var(--color-theme-1) !important;
    }

    :global(.dropdown-menu.show) {
        background-color: var(--background) !important;
        border: none;
        box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }

    /* Remove any transitions that might cause flashing */
    :global(.dropdown *) {
        transition: color 0.2s linear !important;
    }
</style>

