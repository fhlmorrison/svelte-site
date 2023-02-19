<script lang="ts">
    import type { Robot } from "./types";
    export let robotList: Robot[];
    export let robot = robotList[0];
</script>

<select bind:value={robot}>
    {#each robotList as robot}
        <option value={robot}>{robot.name}</option>
    {/each}
</select>
