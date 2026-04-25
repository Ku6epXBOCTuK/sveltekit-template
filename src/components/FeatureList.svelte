<script lang="ts">
	import IconBox from "~icons/lucide/box";
	import IconCheckCircle from "~icons/lucide/check-circle";
	import IconFileCode from "~icons/lucide/file-code";
	import IconFlaskConical from "~icons/lucide/flask-conical";
	import IconPalette from "~icons/lucide/palette";
	import IconSparkles from "~icons/lucide/sparkles";

	const ICON_SIZE = 14;

	const features = [
		{ name: "Svelte 5", desc: "Runes", icon: IconSparkles },
		{ name: "TypeScript", desc: "strict", icon: IconFileCode },
		{ name: "Adapter", desc: "static", icon: IconBox },
		{
			name: "Linting",
			desc: "Prettier + ESLint + Stylelint",
			icon: IconCheckCircle,
		},
		{ name: "Testing", desc: "Vitest + Playwright", icon: IconFlaskConical },
		{ name: "CSS Vars", desc: "linter", icon: IconPalette },
	];
</script>

<section>
	<h2>// Features</h2>
	<ul class="features">
		{#each features as f (f.name)}
			<li>
				<span class="icon"><f.icon size={ICON_SIZE} /></span>
				<span class="name">{f.name}</span>
				<span class="desc">{f.desc}</span>
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
		color: var(--color-green);
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
		display: flex;
		align-items: center;
		gap: 0.5rem;
	}

	.icon {
		color: var(--color-comment);
		display: flex;
	}

	.name {
		color: var(--color-pink);
	}

	.desc {
		color: var(--color-comment);
	}
</style>
