<script>
    export let cardtitle;
    export let desc;
    export let imagesrc;
</script>

<div class="card w-96 bg-base-100 shadow-xl">
    <div class="card-body">
    <h3 class="card-title" >{cardtitle}</h3>
    <p>{desc}</p>
    </div>
    <figure><img src={imagesrc} alt="" /></figure>
</div>

<style>
    .card-body{
        background-color: white;
    }
    .card{
        display: inline-block;
        margin-left: 30px;
        margin-right: 30px;
        margin-bottom: 30px;
        margin-top: 30px;
    }

    .hidden{
        opacity: 0;
        filter: blur(5px);
        transform: translateX(-100%);
        transition: all 1s;
    }
    .show{
        opacity: 1;
        filter: blur(0);
        transform: translateX(0);
    }
</style>