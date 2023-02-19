<script lang="ts">
    import {
        Canvas,
        OrbitControls,
        PerspectiveCamera,
        AmbientLight,
    } from "@threlte/core";
    import { spring } from "svelte/motion";
    import { GLTF } from "@threlte/extras";
    import type { Robot } from "./types";

    const scale = spring(1);

    export let robot: Robot;
</script>

<div>
    <Canvas>
        <PerspectiveCamera position={{ x: 5, y: 2, z: 5 }} fov={25}>
            <OrbitControls autoRotate enableDamping />
        </PerspectiveCamera>

        <AmbientLight />

        <GLTF url={robot.url} useDraco />
    </Canvas>
</div>

<style>
    div {
        height: 100%;
        width: 100%;
    }
</style>
