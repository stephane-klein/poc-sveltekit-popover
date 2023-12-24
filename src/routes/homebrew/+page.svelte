<script>
    import Popover from "./popover.svelte";
</script>

<div class="grid grid-cols-[8em,1fr,8em] grid-rows-[0fr,1fr,0fr] h-screen">
    <div class="text-left"><Popover>Top left</Popover></div>
    <div class="place-self-center"><Popover>Top center</Popover></div>
    <div class="text-right"><Popover>Top right</Popover></div>
    <div class="col-span-3 place-self-center"><Popover>main</Popover></div>
    <div class="text-left"><Popover>Bottom left</Popover></div>
    <div class="place-self-center"><Popover>Bottom center</Popover></div>
    <div class="text-right"><Popover>Bottom right</Popover></div>
</div>
