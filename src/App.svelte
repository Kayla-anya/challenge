<script>
  let name = "Kayla Sookdeosingh"; // Change this to your name
  let bio = "I am a web developer with a passion for building cool things!";
  let hobbies = ["Coding", "Reading", "Traveling"]; // List some hobbies

  
  import Image from "./Image.svelte";
  import Disappearing from "./Disappearing.svelte";
  
</script>

<main>
  <Image />
  <Disappearing />
  
</main>
<div class="container">
  <p>A scrollytelling website by Kayla Sookdeosingh <strong></strong></p>
  <h2>Hope the information was useful!</h2>
  <p class="quote">"Education is the most powerful weapon which you can use to change the world." - Nelson Mandela</p>

  
  
</div>

<style> 
  .quote {
    display: block;
    font-style: italic;
    background: #f9f9f9;
    padding: 1em;
    border-left: 4px solid #0077cc;
    margin: 1em 0;
    animation: fadeIn 2s;
  }

  @keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
  }
</style>
