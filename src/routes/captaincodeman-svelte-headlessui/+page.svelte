<script>
    import Popover from "./popover.svelte";
</script>

<div class="grid grid-cols-[8em,1fr,8em] grid-rows-[0fr,0fr,1fr,0fr] h-screen">
    <!-- start of row1 -->
    <div class="text-left"><Popover>Top left</Popover></div>
    <div class="place-self-center"><Popover>Top center</Popover></div>
    <div class="text-right"><Popover>Top right</Popover></div>
    <!-- start of row2 -->
    <div class="text-left py-4 bg-cyan-600 sticky"><Popover>Fixed left</Popover></div>
    <div class="py-12 bg-cyan-400 text-right sticky"><Popover>Fixed center</Popover></div>
    <div class="text-right py-4 bg-cyan-600 sticky"><Popover>Fixed right</Popover></div>
    <!-- start of row3 -->
    <div class="col-span-3 place-self-center"><Popover>main</Popover></div>
    <!-- start of row4 -->
    <div class="text-left"><Popover>Bottom left</Popover></div>
    <div class="place-self-center"><Popover>Bottom center</Popover></div>
    <div class="text-right"><Popover>Bottom right</Popover></div>
</div>
