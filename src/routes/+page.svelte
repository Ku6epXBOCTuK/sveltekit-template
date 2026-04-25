<script lang="ts">
	import LogoHeader from "$cmp/LogoHeader.svelte";
	import FeatureList from "$cmp/FeatureList.svelte";
	import CommandList from "$cmp/CommandList.svelte";
	import CssVarsInfo from "$cmp/CssVarsInfo.svelte";
	import AppFooter from "$cmp/AppFooter.svelte";
</script>

<main>
	<LogoHeader />
	<FeatureList />
	<CommandList />
	<CssVarsInfo />
	<AppFooter />
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
</style>
