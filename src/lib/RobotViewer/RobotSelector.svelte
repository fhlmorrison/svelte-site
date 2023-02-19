<script lang="ts">
    import type { Robot } from "./types";
    export let robotList: Robot[];
    let robot = robotList[0];
    export let onUpdate: (selected: Robot) => void = (robot) => {
        console.log(`Robot: "${robot.name}" Selected`);
    };
    $: onUpdate(robot);
</script>

<select bind:value={robot}>
    {#each robotList as robot}
        <option value={robot}>{robot.name}</option>
    {/each}
</select>
