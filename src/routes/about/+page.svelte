<script>
    import Navbar from '../../components/Navbar.svelte';
    import sei_img from '../../public/images/IMG_2079.jpg';
    import vball2 from '../../public/images/vball2.jpg';
    import film from '../../public/images/film.jpg';
</script>
  
<main>
    <Navbar />
    <br>
    <div class = "container">
        <h2>About <span id ="me">Me.</span></h2>
        <br>
            <p>
                I am senior at the University of Pittsburgh (Pitt) currently studying Computer Science! I initally enrolled as a bioengineering major at the Swanson School of Engineering at the beginning of 2020. 
                After taking my first programming course as an engineer, I wanted to continue developing and hopefully one day create programs that are more visually appealing than seeing text on the CLI. 
                I had always been the "tech support" person in my household, so I had always enjoyed learning about the different workings of a computer. The following semester, 
                I transferred to the School of Computing and Information and enrolled in the Computer Science program. I always enjoy learning new technologies and figuring out how I can use them in new projects. 
                I am most proficient in Python, Java, Javascript, and SQL!
                <br><br>
                <img src={sei_img} id = "sei" class = "bodyimage" alt = ""/>
                <br><br>
                In the summer of 2023, I interned at SEI Investments as a Software Developer Intern on their SEI Wealth Platform team. During my time here, I had the opportunity to present how SEI could 
                utilize AI tools such as GPT 3.5 and Copilot to enhance developer and back office role efficiency. My project here was to help develop test suites using a end-to-end testing framework called
                Playwright utilizing Typescript. Through this, I was able to learn about the components of our web application by collaborating with developers on creating new features using Angular and Java.
                If you would like to learn more about the impact of my work at SEI, you can read more <a id = "technically" href="https://technical.ly/software-development/sei-cto-zachary-womack-ai/"> here </a>or on my resume!
                <br><br>
                <img src={vball2} id = "vball2" class = "bodyimage" alt = ""/>
                <br><br>
                When I'm not programming, I am playing volleyball! I currently get the opportunity to travel across the country with University of Pittsburgh's Men's Volleyball Club to compete against other schools. 
                Through my experience playing, I learned how to communicate and collaborate as a team. I also enjoy to play volleyball recreationally so on a warm day, you can find me jumping on the Cathedral of Learning Lawn.
                <br><br>
                <img src = {film} class = "bodyimage" alt = "">
                <br><br>
                I also like to shoot photographs on film! I enjoy shooting on an old format like film. This is how I like to express my artistic skills beyond programming!
                <br><br>

            </p>

    </div>
</main>

<style>
    *{
        background-color: white;
    }
    .bodyimage{
        height: auto; 
        width: auto; 
        max-width: 650px; 
        max-height: 650px;

        display: block;
        margin-left: auto;
        margin-right: auto;
        /* width: 50%; */
    }
    @keyframes fadeInAnimation {
    0% {
        opacity: 0;
    }
    100% {
        opacity: 1;
     }
    }
    *{
	    animation: fadeInAnimation ease 2s;
        animation-iteration-count: 1;
    }
    a{
        display: inline;
    }
    #me{
        color:rgb(89, 128, 255);
    }
    #technically{
        color:blue
    }
    p{
        font-size: 1em;
    }
    h2{
        font-size: 3em;
    }
    .container{
        margin-left: auto;
        margin-right: auto;
        padding: 3%;
        position: relative;
        width: 100%;
        max-width: 1000px;
    }
</style>