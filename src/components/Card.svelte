<script>
    export let cardtitle;
    export let desc;
    export let imagesrc;
    export let strings = [];
    export let link;
</script>

<div class="card w-96 bg-base-100 shadow-xl">
    <a href={link}>
    <div class="card-body">
        <h3 class="card-title" >{cardtitle}</h3>
        <p>{desc}</p>
        <div class = "square-image-container ">
            {#each strings as string}

            <img src="{string}" class = 'imagespacing'/>

            {/each}
        </div>
    </div>
    </a>
    <figure><img src={imagesrc} alt="" /></figure>
</div>


<style>
    .imagespacing{
        margin-right: 10px;
    }
    .square-image-container img {
        display: inline-block;
        width: 25px; /* Set the desired width */
        height: 25px; /* Set the same height to maintain square proportion */
    }


    .card-body{
        background-color: white;
    }
    .card:hover {
        transform: translateY(-5px);
    }
    .card{
        transition: all 0.3s ease-out;
        display: inline-block;
        margin-left: 30px;
        margin-right: 30px;
        margin-bottom: 30px;
        margin-top: 30px;
    }
</style>