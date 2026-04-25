<script lang="ts">
	const features = [
		{ name: "Svelte 5", desc: "Runes" },
		{ name: "TypeScript", desc: "strict" },
		{ name: "Adapter", desc: "static" },
		{ name: "Linting", desc: "Prettier + ESLint + Stylelint" },
		{ name: "Testing", desc: "Vitest + Playwright" },
		{ name: "CSS Vars", desc: "linter" },
	];

	const commands = [
		{ cmd: "npm run dev", desc: "dev server" },
		{ cmd: "npm run build", desc: "build static" },
		{ cmd: "npm run preview", desc: "preview" },
		{ cmd: "npm run check", desc: "type check" },
		{ cmd: "npm run lint", desc: "lint all" },
		{ cmd: "npm run test", desc: "run tests" },
	];
</script>

<main>
	<header>
		<pre class="logo">┌─────────────────────────────────────┐
│  SvelteKit Static Template          │
└─────────────────────────────────────┘</pre>
		<p class="subtitle">Template for static sites</p>
	</header>

	<section>
		<h2>// Features</h2>
		<ul class="features">
			{#each features as f (f.name)}
				<li><span class="name">{f.name}</span> <span class="desc">{f.desc}</span></li>
			{/each}
		</ul>
	</section>

	<section>
		<h2>// Commands</h2>
		<ul class="commands">
			{#each commands as c (c.cmd)}
				<li><code>{c.cmd}</code> <span class="desc">{c.desc}</span></li>
			{/each}
		</ul>
	</section>

	<section>
		<h2>// CSS Variables Linter</h2>
		<p>Проверяет CSS-переменные: ошибка если используется но не определена.</p>
		<pre><code>npm run lint:css-vars</code></pre>
	</section>

	<footer>
		<p>Node.js >= 22.0.0</p>
	</footer>
</main>

<style>
	:global(body) {
		background: #1a1a1a;
		color: #e0e0e0;
		font-family: "JetBrains Mono", "Fira Code", "Consolas", monospace;
		font-size: 14px;
		line-height: 1.6;
		margin: 0;
		padding: 2rem;
	}

	main {
		max-width: 600px;
		margin: 0 auto;
	}

	header {
		margin-bottom: 2rem;
	}

	.logo {
		background: #0d0d0d;
		padding: 1rem;
		border: 1px solid #333;
		overflow-x: auto;
		color: #00ff00;
	}

	.subtitle {
		color: #666;
		margin-top: 0.5rem;
	}

	section {
		margin-bottom: 1.5rem;
	}

	h2 {
		font-size: 1rem;
		color: #00ff00;
		margin-bottom: 0.5rem;
		font-weight: normal;
	}

	.features {
		list-style: none;
		padding: 0;
		margin: 0;
	}

	.features li {
		padding: 0.25rem 0;
	}

	.features .name {
		color: #ff79c6;
	}

	.features .desc {
		color: #6272a4;
	}

	.commands {
		list-style: none;
		padding: 0;
		margin: 0;
	}

	.commands li {
		padding: 0.25rem 0;
	}

	code {
		background: #0d0d0d;
		padding: 0.2rem 0.4rem;
		border: 1px solid #333;
		color: #8be9fd;
	}

	.commands .desc {
		color: #6272a4;
		margin-left: 0.5rem;
	}

	pre {
		background: #0d0d0d;
		padding: 1rem;
		border: 1px solid #333;
		overflow-x: auto;
	}

	footer {
		margin-top: 2rem;
		padding-top: 1rem;
		border-top: 1px solid #333;
		color: #6272a4;
	}
</style>