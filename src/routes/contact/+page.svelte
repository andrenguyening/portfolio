
<script>
    import ContactForm from '../../components/ContactForm.svelte';
    import Navbar from '../../components/Navbar.svelte';

  </script>
  <Navbar />
  <div class = "container">
    <div class="content">
        <h1>Contact Us</h1>
        <p>Please fill out the form below to get in touch with us.</p>
        <ContactForm />
    </div>
  </div>
  
  <style>
    h1{
        font-size: 2em;
    }
    h1,p{
        text-align: center;
    }
       .container{
        max-width: fit-content;
        margin-left: auto;
        margin-right: auto;
        /* background-color: blue; */
        padding: 3%;
        position: relative;
        width: 100%;
        max-width: 1000px;
        height:1000px;
    }


    /* Media query for smaller screens */
    @media (max-width: 768px) {
    .content {
      max-width: 90%; /* Adjust the maximum width for smaller screens */
    }
  }
  </style>