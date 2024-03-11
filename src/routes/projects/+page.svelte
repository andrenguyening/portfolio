<script>
    import Navbar from '../../components/Navbar.svelte';
    import { fly } from 'svelte/transition';
    import Card from '../../components/Card.svelte';
    function toggleVisibility(card) {
        card.visible = !card.visible;
    }
  let cards = [
    { id: 1, cardtitle: 'Card 1', desc: 'Content for Card 1' ,imagesrc:"https://daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.jpg"},
    { id: 2, cardtitle: 'Card 2', desc: 'Content for Card 2',imagesrc:"https://daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.jpg" },
    { id: 3, cardtitle: 'Card 3', desc: 'Content for Card 2',imagesrc:"https://daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.jpg" },
    { id: 4, cardtitle: 'Card 4', desc: 'Content for Card 2',imagesrc:"https://daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.jpg" },
    // Add more cards as needed
  ];
</script>
<Navbar />
<div class= "container">
    <h1 id= "title">Projects I've Worked On</h1>
    <br><br><br>
    <div class = "card-container" >
        {#each cards as card (card.id)}
            <Card cardtitle= {card.cardtitle} desc={card.desc} imagesrc = {card.imagesrc}/>
        {/each}
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
        display: flex;
        margin-left: auto;
        margin-right: auto;
        align-items: flex-start;
        width: 100%;
        height:800px;
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