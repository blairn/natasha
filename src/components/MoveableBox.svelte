<script>
    import EditableLabel from "./EditableLabel.svelte";
    export var x=0;
    export var y=0;

    var panning = false;
    function startpan(){
        panning=true
    }

    function mousemove(e) {
        if (panning) {
            x = event.clientX;
            y = event.clientY;
            console.log(e)
        }
    }

    function stoppan(){
        panning=false
    }


</script>

<style>
    .box {
        position: absolute;
        background-color: rgba(255, 255, 255, .15);
        backdrop-filter: blur(3px);

    }

    .label {
        padding: 2px;
        background-color:black;
        color:white;
    }

    .move {
        padding-right: 5px;
    }
</style>

<div class="box" width="50px" style="left:{x}px; top:{y}px">
    <div class="label"><i class="fa fa-arrows move" aria-hidden="true" on:mousedown={startpan} on:mouseup={stoppan} on:mousemove={mousemove}></i><slot name="label"><EditableLabel label="Default Label"></EditableLabel></slot></div>
    <div class="body"><slot name="body">Default Body</slot></div>
    <div class="footer"><slot name="footer">Default Footer</slot></div>
</div>

