<script>
  import Canvas from './Canvas.svelte';
  import CanvasCoordOverlay from './CanvasCoordOverlay.svelte';
  let canvas_coord = {
    x: 0,
    y: 0
  };
</script>

<div>
    <section class="canvas-space">
        <div class="canvas-container">
            <Canvas bind:coord={canvas_coord}></Canvas>
        </div>
    </section>
</div>
<CanvasCoordOverlay bind:coord={canvas_coord} />

<style>

    .canvas-space {
        display: flex;
        /* flex-flow: column; */
        height: 94vh;
        width: 100vw;
        justify-content: center;
        align-items: center;
    }
    .canvas-container {
        /* margin-top: 8%; */
        display: flex;
        justify-content: center;
        align-content: center;
        width: 75%;
        /* flex: 1; */
    }

</style>