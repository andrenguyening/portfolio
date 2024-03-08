<head>
	<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&display=swap" rel="stylesheet">
	<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css" integrity="sha512-DTOQO9RWCH3ppGqcWaEA1BIZOC6xxalwEsw9c2QQeAIftl+Vegovlnee1c9QX4TctnWMn13TZye+giMm8e2LwA==" crossorigin="anonymous" referrerpolicy="no-referrer" />
</head>

<script>
	import Navbar from './Navbar.svelte';
</script>


<main>
	<Navbar />
	<div class = "container">
		<h1>I am Andre Nguyen<span id="period">.</span></h1>
		<p>I am a student studying Computer Science at the University of Pittsburgh! I love learning new technologies and developing cool projects! I specialize in Python, Java, and Full Stack Development. I am currently seeking full-time software developer roles. </p>
		<div class = "socials">
            <a href="https://www.linkedin.com/in/andre-nguyen-79b5a2217/"><i class="fa-brands fa-linkedin"></i></a>		
            <a href="https://github.com/andrenguyening"><i class="fa-brands fa-github"></i></a>	
			<a href="mailto:andre.l.nguyen@outlook.com"><i class="fa-solid fa-envelope"></i></a>
		</div>
	</div>
	<img id="pp" src = "public\images\image2.jpg" alt = "">


</main>

<style>
*{
	animation: fadeInAnimation ease 2s;
    animation-iteration-count: 1;
}

/*		ids		*/
#pp{
	float: right;
	margin-right: 23%;
	margin-top: -36%;
    height: auto; 
    width: auto; 
    max-width: 550px; 
    max-height: 550px;
	clip-path: circle();
}
#period{
	color:rgb(89, 128, 255);
}


/*		classes		*/

.fa-linkedin:hover {
            animation: fa-beat 1s ;
        }
.fa-github:hover {
    animation: fa-beat 1s ;
}
.fa-envelope:hover {
    animation: fa-beat 1s ;
}
.container{
	display: flex;
	flex-direction: column;
	justify-content: center;
	height: 100vh;
	margin-left: 20%;
	/* background-color:blue; */
	width:800px
}

.socials{
	font-size: 30px;
	/* background-color: red; */
	/* justify-content: center;
	margin-left: 300px;
	width:225px */
}

/*		tag css		*/
h1 {
	font-size: 5em;
	margin: 0;
	
}
a{
    display: inline-block;
}
i{
	padding-right: 40px;
}
p {
	margin: 1;
	width: 850px;
}

/*	animations	*/
@keyframes fadeInAnimation {
    0% {
        opacity: 0;
    }
    100% {
        opacity: 1;
     }
}

</style>