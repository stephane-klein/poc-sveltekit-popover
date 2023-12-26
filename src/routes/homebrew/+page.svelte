<script>
    import Popover from "./popover.svelte";
</script>

<div class="grid grid-cols-[8em,1fr,8em] grid-rows-[0fr,0fr,1fr,0fr] h-screen max-h-screen">
    <!-- start of row1 -->
    <div class="text-left"><Popover>Top left</Popover></div>
    <div class="place-self-center"><Popover>Top center</Popover></div>
    <div class="text-right"><Popover>Top right</Popover></div>
    <!-- start of row2 -->
    <div class="text-left py-4 bg-cyan-600"><Popover><div class="sticky">Fixed left</div></Popover></div>
    <div class="py-12 bg-cyan-400 text-right"><Popover><div class="sticky">Fixed center</div></Popover></div>
    <div class="text-right py-4 bg-cyan-600"><Popover><div class="sticky">Fixed right</div></Popover></div>
    <!-- start of row3 -->
    <div class="col-span-3 relative">
        <table role="table" class="overflow-scroll grid grid-cols-[1fr,0fr,0fr,0fr] absolute w-full h-full top-0">
            <thead class="contents">
                <tr role="row" class="contents">
                    <th role="columnheader" class="sticky top-0 py-12 px-4 bg-fuchsia-400">
                        <Popover>Column A</Popover>
                    </th>
                    <th role="columnheader" class="sticky top-0 py-12 px-4 bg-fuchsia-600">
                        <Popover>Column B</Popover>
                    </th>
                    <th role="columnheader" class="sticky top-0 py-12 px-4 bg-fuchsia-400">
                        <Popover>Column C</Popover>
                    </th>
                    <th role="columnheader" class="sticky top-0 py-12 px-4 bg-fuchsia-600">
                        <Popover>Column D</Popover>
                    </th>
                </tr>
            </thead>
            <tbody class="contents">
                {#each Array(100) as _, i}
                    <tr role="row" class="contents">
                        <td role="cell">{i} - a</td>
                        <td role="cell">{i} - b</td>
                        <td role="cell">{i} - c</td>
                        <td role="cell">{i} - d</td>
                    </tr>
                {/each}
            </tbody>
        </table>
    </div>
    <!-- start of row4 -->
    <div class="col-span-3 place-self-center"><Popover>main</Popover></div>
    <!-- start of row5 -->
    <div class="text-left"><Popover>Bottom left</Popover></div>
    <div class="place-self-center"><Popover>Bottom center</Popover></div>
    <div class="text-right"><Popover>Bottom right</Popover></div>
</div>
