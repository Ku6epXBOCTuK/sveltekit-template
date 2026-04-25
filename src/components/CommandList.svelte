<script lang="ts">
	const commands = [
		{ cmd: "npm run dev", desc: "dev server" },
		{ cmd: "npm run build", desc: "build static" },
		{ cmd: "npm run preview", desc: "preview" },
		{ cmd: "npm run check", desc: "type check" },
		{ cmd: "npm run lint", desc: "lint all" },
		{ cmd: "npm run test", desc: "run tests" },
	];
</script>

<section>
	<h2>// Commands</h2>
	<ul class="commands">
		{#each commands as c (c.cmd)}
			<li><code>{c.cmd}</code> <span class="desc">{c.desc}</span></li>
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
</style>
