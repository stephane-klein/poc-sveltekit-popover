<script lang="ts">
    import { onMount } from "svelte";
    import { createPopover } from "svelte-headlessui";
    import { createPopperActions } from "svelte-popperjs";

    const popover = createPopover({});

    const [popperRef, popperContent] = createPopperActions({
        placement: "bottom"
    });
    const extraOpts = {
        modifiers: [{ name: "offset", options: { offset: [0, 8] } }]
    };
    let panel;
    onMount(() => {
        document.getElementsByTagName("body")[0].append(panel);
    });
</script>

<button use:popover.button use:popperRef>
    <slot />
</button>

<div bind:this={panel}>
    {#if $popover.expanded}
        <div
            use:popover.panel
            use:popperContent={extraOpts}
            class="w-56 shrink rounded-xl bg-white p-4 text-sm font-semibold leading-6 text-gray-900 shadow-lg ring-1 ring-gray-900/5 text-left"
        >
            <p>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. In quis neque commodo, congue dui rutrum,
                pellentesque risus. Suspendisse potenti. Curabitur maximus mi sit amet gravida hendrerit. Nullam
                sollicitudin imperdiet nunc, eget feugiat tortor ullamcorper iaculis. Suspendisse dictum convallis metus
                sit amet tincidunt.
            </p>
        </div>
    {/if}
</div>
