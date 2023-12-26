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
        <div
            class="w-56 shrink rounded-xl bg-white p-4 text-sm font-semibold leading-6 text-gray-900 shadow-lg ring-1
            ring-gray-900/5 text-left"
            data-popper-arrow
        >
            <p>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. In quis neque commodo, congue dui rutrum,
                pellentesque risus. Suspendisse potenti. Curabitur maximus mi sit amet gravida hendrerit. Nullam
                sollicitudin imperdiet nunc, eget feugiat tortor ullamcorper iaculis. Suspendisse dictum convallis metus
                sit amet tincidunt.
            </p>
        </div>
    </div>
{/if}
