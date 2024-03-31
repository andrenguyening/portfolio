<script>
    import Navbar from '../../components/Navbar.svelte';
    import Card from '../../components/Card.svelte';
    import budgetimg from '../../public/images/budget.jpg';
    import portimg from '../../public/images/port.jpg';
    import chatimg from '../../public/images/chat.jpg';
    import irisimg from '../../public/images/iris.jpg'

    let iris = [
    "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/python/python-original.svg",
    "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/flask/flask-original.svg",
    "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/javascript/javascript-original.svg",
    "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/html5/html5-original.svg"

    ]
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

    let links = ["https://github.com/andrenguyening/ChatApp",
    "https://github.com/andrenguyening/BudgetApp",
    "https://github.com/andrenguyening/portfolio", 
    "https://devpost.com/software/iris-an-llm-based-browser-navigation?ref_content=my-projects-tab&ref_feature=my_projects"
    ];


    let cards = [
        { id: 3, cardtitle: 'Iris: LLM Internet Navigation', desc: 'LLM browser control for people with visual impairments!', strings: iris, link:links[3]},
        { id: 2, cardtitle: 'Portfolio Website', desc: 'My personal website to introduce myself! Learn and read more about me here!', strings: portfolio, link:links[2]},
        { id: 1, cardtitle: 'Budgify', desc: 'Track your spending! A budget tracking application using a RESTful API and React!' ,strings: budget, link:links[1]},
        { id: 0, cardtitle: 'Conversate', desc: 'Chat with your friends! Chatroom app with live chatting utilizing AJAX polling and updating!', strings:chat, link:links[0]},
    ];

    let cardimgs = [portimg,budgetimg,chatimg,irisimg]


</script>
<Navbar />
<div class= "container">
    <h1 id= "title">Projects I've Worked On</h1>
    <br><br><br>
    <div class = "card-container" >
        {#each cards as card (card.id)} 
            <Card cardtitle= {card.cardtitle} desc={card.desc} imagesrc = {cardimgs[card.id]} strings={card.strings} link = {card.link}/>
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