<script lang="ts">
	import IconEye from "~icons/lucide/eye";
	import IconFileCheck from "~icons/lucide/file-check";
	import IconBuild from "~icons/lucide/hammer";
	import IconPlay from "~icons/lucide/play";
	import IconScan from "~icons/lucide/scan";
	import IconTestTube from "~icons/lucide/test-tube";

	const ICON_SIZE = 14;

	const commands = [
		{ cmd: "npm run dev", desc: "dev server", icon: IconPlay },
		{ cmd: "npm run build", desc: "build static", icon: IconBuild },
		{ cmd: "npm run preview", desc: "preview", icon: IconEye },
		{ cmd: "npm run check", desc: "type check", icon: IconFileCheck },
		{ cmd: "npm run lint", desc: "lint all", icon: IconScan },
		{ cmd: "npm run test", desc: "run tests", icon: IconTestTube },
	];
</script>

<section>
	<h2>// Commands</h2>
	<ul class="commands">
		{#each commands as c (c.cmd)}
			<li>
				<span class="icon"><c.icon size={ICON_SIZE} /></span>
				<code>{c.cmd}</code>
				<span class="desc">{c.desc}</span>
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

	.commands {
		list-style: none;
		padding: 0;
		margin: 0;
	}

	.commands li {
		padding: 0.25rem 0;
		display: flex;
		align-items: center;
		gap: 0.5rem;
	}

	.icon {
		color: var(--color-comment);
		display: flex;
	}

	code {
		background: var(--color-code-bg);
		padding: 0.2rem 0.4rem;
		border: 1px solid var(--color-border);
		color: var(--color-blue);
	}

	.commands .desc {
		color: var(--color-comment);
	}
</style>
