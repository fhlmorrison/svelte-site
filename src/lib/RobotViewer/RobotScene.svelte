<script lang="ts">
    import {
        Canvas,
        OrbitControls,
        PerspectiveCamera,
        AmbientLight,
    } from "@threlte/core";
    import { GLTF } from "@threlte/extras";
    import type { Robot } from "./types";

    export let robot: Robot;
    let loaded = true;
    const setLoading = (val) => {
        loaded = val;
    };
    $: setLoading(!robot);
</script>

<div>
    <Canvas>
        <PerspectiveCamera position={{ x: 5, y: 2, z: 5 }} fov={25}>
            <OrbitControls autoRotate enableDamping />
        </PerspectiveCamera>

        <AmbientLight />

        <GLTF url={robot.url} useDraco on:load={() => (loaded = true)} />
    </Canvas>
    {#if !loaded}
        <span>Loading...</span>
    {:else}
        <span>{robot && robot.name}</span>
    {/if}
</div>

<style>
    div {
        height: 100%;
        width: 100%;
    }
</style>
