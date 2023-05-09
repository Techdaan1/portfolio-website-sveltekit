<script>
  let user = { mode: false };

  function toggle() {
    user.mode = !user.mode;
  }
</script>

<svelte:head>
  <title>Contact</title>
</svelte:head>

<div class="contact-container">
  <h1>Danielle Neeleman</h1>
  <a href="mailto:daantjen@hotmail.com">daantjen@hotmail.com</a>,
  <div class="social-media">
    <a
      href="https://www.linkedin.com/in/danielle-neeleman-641a5a2a/"
      target="_blank"
    >
      <img src="/linkedin-icon.png" alt="Linkedin account Danielle" /></a
    >
    <a href="https://www.instagram.com/danielle_neeleman/" target="_blank">
      <img src="/instagram-icon.png" alt="Instagram account Danielle" /></a
    >
    <a href="https://www.facebook.com/danielle.neeleman/" target="_blank">
      <img src="/facebook-icon.png" alt="Facebook account Danielle" /></a
    >
  </div>
  <div class="inpirational-words">
    {#if user.mode}
      <button class="button1" on:click="{toggle}">
        Enjoy the small things
      </button>
    {:else}
      <button class="button2" on:click="{toggle}"> Have a great day! </button>
    {/if}
  </div>
</div>

<style>
  .button1 {
    background-color: pink;
    margin-top: 50px;
    padding: 20px;
    border-radius: 50%;
    border: none;
    font-family: "Lucida Handwriting", "Courier New", monospace;
    cursor: pointer;
    transition: 0.7s ease;
  }

  .button1:hover,
  .button2:hover {
    color: red;
  }

  .button2 {
    background-color: lightgreen;
    margin-top: 50px;
    padding: 20px;
    border-radius: 50%;
    border: none;
    font-family: "Lucida Handwriting", "Courier New", monospace;
    cursor: pointer;
    transition: 0.7s ease;
  }

  img {
    margin-top: 50px;
    height: 70px;
  }

  .contact-container {
    font-family: "Lucida Handwriting", "Courier New", monospace;
    max-width: 1400px;
    margin: 100px auto;
    padding: 0 10% 0 10%;
    text-align: center;
  }
</style>
