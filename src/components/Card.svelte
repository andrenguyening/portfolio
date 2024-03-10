<scipt>
    let cardtitle = "";
    let desc = "";
    let imagesrc = ""
</scipt>

<div class="card w-96 bg-base-100 shadow-xl">
    <div class="card-body">
    <h3 class="card-title" >"{cardtitle}"</h3>
    <p>{desc}</p>
    </div>
    <figure><img src={imagesrc} alt="" /></figure>
</div>

<style>
    .card-body{
        background-color: white;
    }
</style>