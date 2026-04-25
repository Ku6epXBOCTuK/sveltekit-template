<script lang="ts">
	import AppFooter from "$cmp/AppFooter.svelte";
	import CommandList from "$cmp/CommandList.svelte";
	import CssVarsInfo from "$cmp/CssVarsInfo.svelte";
	import FeatureList from "$cmp/FeatureList.svelte";
	import LogoHeader from "$cmp/LogoHeader.svelte";
</script>

<main>
	<LogoHeader />
	<FeatureList />
	<CommandList />
	<CssVarsInfo />
	<AppFooter />
</main>
