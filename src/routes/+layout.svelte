<script lang="ts">
	import "./layout.css";
	import favicon from "#lib/assets/614d1097-0a5e-4738-8119-975b124dd369.ico";
	import type { LayoutProps } from "./$types";

	let { children }: LayoutProps = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

{@render children()}
