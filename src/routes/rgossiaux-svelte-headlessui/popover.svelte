<script>
    import { Popover, PopoverButton, PopoverPanel } from "@rgossiaux/svelte-headlessui";
</script>

<Popover style="position: relative;">
    <PopoverButton><slot /></PopoverButton>

    <PopoverPanel style="position: absolute; z-index: 10;">
        <div
            class="w-56 shrink rounded-xl bg-white p-4 text-sm font-semibold leading-6 text-gray-900 shadow-lg ring-1
            ring-gray-900/5 text-left"
        >
            <p>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. In quis neque commodo, congue dui rutrum,
                pellentesque risus. Suspendisse potenti. Curabitur maximus mi sit amet gravida hendrerit. Nullam
                sollicitudin imperdiet nunc, eget feugiat tortor ullamcorper iaculis. Suspendisse dictum convallis metus
                sit amet tincidunt.
            </p>
        </div>
    </PopoverPanel>
</Popover>
