<script>
</script>

  <head>
	<!-- <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&display=swap" rel="stylesheet"> -->
	<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css" integrity="sha512-DTOQO9RWCH3ppGqcWaEA1BIZOC6xxalwEsw9c2QQeAIftl+Vegovlnee1c9QX4TctnWMn13TZye+giMm8e2LwA==" crossorigin="anonymous" referrerpolicy="no-referrer" />
</head>

  <nav>
	<div>
	  <h1><div class = "typing">Hi, I'm <span id = "name">Andre</span></div></h1>
	</div>
	<div>
		<ul>
		  <li><a href="/"><i class="fa-solid fa-house" id = "house"></i><span class= "iconlabel">Home</span></a></li>
		  <li><a href="/about"><i class="fa-solid fa-user"></i><span class= "iconlabel">About</span></a></li>
		  <li><a href="/projects"><i class="fa-solid fa-code"></i><span class= "iconlabel">Projects</span></a></li>
		  <li><a href="#">Resume</a></li>
		  <li><a href="#">Blog</a></li>
		  <li><a href="#">Contact</a></li>
		</ul>
	</div>
  </nav>

  <style>
    /* Your styling for the navbar goes here */
    #name{
        color:rgb(89, 128, 255);
    }
    
    nav {
        display: flex;
        justify-content: space-between;
        align-items: center;
        border-bottom: 2px solid #e0e0e0; /* Add a border to the bottom */
    }
    
    ul {
        list-style: none;
        display: flex;
    }
    
    li {
        margin-right: 15px;
    }
    
    .iconlabel{
        padding-left: 7px;
    }
    .typing {
      /* font-family: "Roboto", sans-serif; */
      padding-left: 30px;
      width: 14ch;
      animation: typing 2s steps(13), blink .5s step-end 2s infinite alternate;
      white-space: nowrap;
      overflow: hidden;
      border-right: 3px solid;
      font-size: 1em;
    }
    
    @keyframes typing {
      from {
        width: 0;
      }
    }
    
    @keyframes blink {
      50% {
        border-color: transparent;
      }
    }
    
    @keyframes backspace {
      to {
        width: 0;
      }
    }
    
    </style>