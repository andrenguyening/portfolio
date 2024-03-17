<!-- ContactForm.svelte -->
<script>
    let name = '';
    let email = '';
    let message = '';
    let submissionStatus = '';
  
    async function handleSubmit(event) {
      event.preventDefault();
      
      // Perform form validation here if needed
      
      // Simulate a submission delay (remove this in a real application)
      await new Promise(resolve => setTimeout(resolve, 1000));
  
      // Here you can implement your logic to handle form submission,
      // such as sending data to a server or displaying a confirmation message.
      console.log('Name:', name);
      console.log('Email:', email);
      console.log('Message:', message);
  
      // Display submission success message
      submissionStatus = 'Message sent!';
      
      // Clear form fields after successful submission
      name = '';
      email = '';
      message = '';
    }
  </script>
  
  <div class = "container">
    {#if submissionStatus}
      <p>{submissionStatus}</p>
    {/if}
  
    <form on:submit={handleSubmit}>
      <label>
        Name:
        <input type="text" bind:value={name} required />
      </label>
      <label>
        Email:
        <input type="email" bind:value={email} required />
      </label>
      <label>
        Message:
        <textarea bind:value={message} required></textarea>
      </label>
      <button type="submit">Send Message</button>
    </form>
</div>

<style>
    .container{
    max-width: fit-content;
    margin-left: auto;
    margin-right: auto;
    /* background-color: red; */
    padding: 3%;
    position: relative;
    width: 100%;
    max-width: 1000px;
    height:1000px;
}
</style>