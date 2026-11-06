<script lang="ts">
    import type { Snippet } from "svelte";
    import type {
        HTMLAnchorAttributes,
        HTMLButtonAttributes
    } from "svelte/elements";

    type ButtonProps = HTMLButtonAttributes & {
        as?: "button";
        children: Snippet;
    };
    type AnchorProps = HTMLAnchorAttributes & {
        as: "a";
        children: Snippet;
    };
    type Props = ButtonProps | AnchorProps;

    let { as = "button", children, class: className, ...rest }: Props =
        $props();
</script>

<svelte:element this={as} {...rest} class="btn {className}">
    {@render children()}
</svelte:element>

<style>
    .btn {
        background-color: var(--color-zinc-950);
        border-width: 1px;
        border-color: var(--color-zinc-900);
        font-size: var(--text-base);
        line-height: var(--text-base--line-height);
        border-radius: var(--radius-sm);
        color: var(--color-zinc-50);
        padding: calc(var(--spacing) * 1.5);
        font-family: var(--font-sans);
    }

    .btn[data-variant="outline"] {
        background-color: var(--color-white);
        color: var(--color-black);
        line-height: var(--text-base--line-height);
        font-size: var(--text-base);
        border-width: 1px;
        border-radius: var(--radius-sm);
        font-family: var(--font-sans);
        padding: calc(var(--spacing) * 1.5);
        border-color: var(--color-zinc-300);
    }
</style>
