<script>
    import { createPopperActions } from "svelte-popperjs";
    const [popperRef, popperContent] = createPopperActions({
        placement: "bottom"
    });
    const extraOpts = {
        modifiers: [{ name: "offset", options: { offset: [0, 8] } }]
    };

    let showTooltip = false;
</script>

<button use:popperRef on:click={() => (showTooltip = true)}>
    <slot />
</button>
{#if showTooltip}
    <div id="tooltip" use:popperContent={extraOpts}>
        My tooltip
        <div id="arrow" data-popper-arrow />
    </div>
{/if}
