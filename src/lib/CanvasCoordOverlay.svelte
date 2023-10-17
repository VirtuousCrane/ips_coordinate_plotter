<script>
    export let coord = {
        x: 0,
        y: 0
    };
</script>

<div class="overlay">
    <div class="content-container">
        <p>x: {Math.round(coord.x)}&nbsp;&nbsp;&nbsp;y: {Math.round(coord.y)}</p>
    </div>
</div>

<style>
    .overlay {
        position: fixed;
        width: 200px;
        height: 50px;
        bottom: 0;
        z-index: 2;
        background-color: #d9d9d9;
    }
    
    .content-container {
        position: relative;
        text-align: center;
    }
</style>
