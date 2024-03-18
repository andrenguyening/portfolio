<script>
    import Navbar from '../../components/Navbar.svelte';
    import Card from '../../components/Card.svelte';
    import budgetimg from '../../public/images/budget.jpg';

    let portfolio = ["https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/svelte/svelte-original.svg",
    "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/javascript/javascript-original.svg",
    "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/html5/html5-original.svg"
    ];
    
    let budget = ["https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/react/react-original.svg",
    "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/javascript/javascript-original.svg",
    "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/python/python-original.svg",
    "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/flask/flask-original.svg"];

    let chat = ["https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/javascript/javascript-original.svg",
    "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/html5/html5-original.svg",
    "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/python/python-original.svg",
    "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/flask/flask-original.svg"
    ];

    let links = ["https://github.com/andrenguyening/portfolio","https://github.com/andrenguyening/BudgetApp",
    "https://github.com/andrenguyening/ChatApp",
    "https://github.com/andrenguyening/portfolio",
    ];


    let cards = [
        { id: 1, cardtitle: 'Portfolio Website', desc: 'Personal website to introduce myself! Check me out!' ,imagesrc:'../../src/public/images/port.jpg', strings: portfolio, link:links[0]},
        { id: 2, cardtitle: 'Budgify', desc: 'A budget tracking app using a custom RESTful API!',imagesrc:"../../src/public/images/budget.jpg" ,strings: budget, link:links[1]},
        { id: 3, cardtitle: 'Conversate', desc: 'Chatroom app with live chatting utilizing AJAX polling and updating!',imagesrc:"../../src/public/images/chat.jpg", strings:chat, link:links[2]},
        // { id: 4, cardtitle: 'Card 4', desc: 'Content for Card 2',imagesrc:"https://daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.jpg", link: links[3]}
        // Add more cards as needed
    ];


</script>
<Navbar />
<div class= "container">
    <h1 id= "title">Projects I've Worked On</h1>
    <br><br><br>
    <div class = "card-container" >
        {#each cards as card (card.id)} 
            <Card cardtitle= {card.cardtitle} desc={card.desc} imagesrc = {card.imagesrc} strings={card.strings} link = {card.link}/>
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