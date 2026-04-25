<script lang="ts">
	const features = [
		{ name: "Svelte 5", desc: "Runes" },
		{ name: "TypeScript", desc: "strict" },
		{ name: "Adapter", desc: "static" },
		{ name: "Linting", desc: "Prettier + ESLint + Stylelint" },
		{ name: "Testing", desc: "Vitest + Playwright" },
		{ name: "CSS Vars", desc: "linter" },
	];
</script>

<section>
	<h2>// Features</h2>
	<ul class="features">
		{#each features as f (f.name)}
			<li>
				<span class="name">{f.name}</span> <span class="desc">{f.desc}</span>
			</li>
		{/each}
	</ul>
</section>

<style>
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
</style>
