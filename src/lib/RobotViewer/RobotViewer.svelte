<script lang="ts">
    import type { Robot } from "./types";
    import RobotScene from "./RobotScene.svelte";
    import RobotSelector from "./RobotSelector.svelte";
    const robotList: Robot[] = [
        {
            name: "RoadRunner",
            url: "src/assets/RoadRunner_Compressed.draco.glb",
        },
        { name: "2020", url: "src/assets/2020_Compressed.draco.glb" },
    ];
    let robot;
    let onUpdate = (selected: Robot) => {
        robot = selected;
    };
</script>

<div>
    <div>Select a robot to view</div>
    <RobotSelector {robotList} {onUpdate} />
    <RobotScene {robot} />
</div>
