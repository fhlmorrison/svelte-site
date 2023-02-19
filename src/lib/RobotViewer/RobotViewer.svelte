<script lang="ts">
    import type { Robot } from "./types";
    import RobotScene from "./RobotScene.svelte";
    import RobotSelector from "./RobotSelector.svelte";
    const robotList: Robot[] = [
        {
            name: "RoadRunner",
            url: "/models/RoadRunner_Compressed.draco.glb",
        },
        { name: "2020", url: "/models/2020_Compressed.draco.glb" },
    ];
    let robot;
</script>

<div>
    <div>Select a robot to view</div>
    <RobotSelector {robotList} bind:robot />

    <RobotScene {robot} />
</div>
