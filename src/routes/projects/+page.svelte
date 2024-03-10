<script>
    import Navbar from '../../components/Navbar.svelte';
</script>
<Navbar />
<div class= "container">
    <h1 id= "title">Projects I've Worked On</h1>
    <br>    <br>
    <br>
    <div class = "card-container">
        <div class="card w-96 bg-base-100 shadow-xl">
            <div class="card-body" style="background-color:white ">
            <h3 class="card-title" >Budgify</h3>
            <p>Manage your budget! Created using Javascript, React, Python, and Flask</p>
            </div>
            <figure><img src="https://daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.jpg" alt="Shoes" /></figure>
        </div>
        <div class="card w-96 bg-base-100 shadow-xl">
            <div class="card-body" style="background-color:white ">
            <h3 class="card-title" >Chat App</h3>
            <p>Come chat! Created with using Javascript, Python, Flask, and AJAX</p>
            </div>
            <figure><img src="https://daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.jpg" alt="Shoes" /></figure>
        </div>
        <div class="card w-96 bg-base-100 shadow-xl">
            <div class="card-body" style="background-color:white ">
            <h3 class="card-title" >Budgify</h3>
            <p>Manage your budget! Created using React, Python, Flask</p>
            </div>
            <figure><img src="https://daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.jpg" alt="Shoes" /></figure>
        </div>
        <div class="card w-96 bg-base-100 shadow-xl">
            <div class="card-body" style="background-color:white ">
            <h3 class="card-title" >Budgify</h3>
            <p>Manage your budget! Created using Javascript, React, Python, and Flask</p>
            </div>
            <figure><img src="https://daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.jpg" alt="Shoes" /></figure>
        </div>
    </div>
</div>

<style>
    @keyframes fadeInAnimation {
    0% {
        opacity: 0;
    }
    100% {
        opacity: 1;
     }
    }

    #title{
        font-size: 3em;
    }
    .container{
        animation: fadeInAnimation ease 2s;
        animation-iteration-count: 1;
        place-content:center;
        place-items: center;
        max-width: fit-content;
        margin-left: auto;
        margin-right: auto;
        /* background-color: blue; */
        padding: 3%;
        position: relative;
        width: 100%;
        max-width: 1500px;
        /* height:1000px; */
    }
    .card-container{
        /* background-color: red; */
        /* margin-left: auto;
        margin-right: auto; */
        place-content:center;
        place-items: center;
        max-width: fit-content;
        margin-left: auto;
        margin-right: auto;
        position: relative;
        width: 100%;
        height:1000px;
    }
    .card{
        display: inline-block;
        /* padding: 15px; */
        margin-left: 30px;
        margin-right: 30px;
        margin-bottom: 30px;
        margin-top: 30px;
    }
</style>