<script>
    export let coord = {
        x: 0,
        y: 0
    };
    let canvas, ctx;
    
    // Gets called when mouse cursor moved on canvas
    function handleMove(event) {
        let rect = canvas.getBoundingClientRect();
        coord.x = event.clientX - rect.left;
        coord.y = event.clientY - rect.top;
        console.log(coord);
    }
    
    // Gets called when canvas is created
    function createCanvasCallback(node) {
        canvas = node;
        ctx = canvas.getContext("2d");
    }
</script>

<canvas on:pointermove={handleMove} use:createCanvasCallback></canvas>

<style>
    canvas {
        background-color: aqua;
        width: 100%;
        height: 75%;
    }
</style>

