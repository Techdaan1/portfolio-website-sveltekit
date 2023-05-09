<svelte:head>
  <title>Danielle Neeleman</title>
</svelte:head>

<div class="container">
  <img
    src="\danielle_neeleman.jpg"
    alt="picture_danielle"
    class="profile-picture"
  />
  <p>
    Hey Everyone 👋! Welcome to my portfolio website. My name is Danielle
    Neeleman and I am a Dutch web developer living in Berlin. Take a seat and
    have fun exploring my work. If you have any questions please do not hesitate
    to contact me.
  </p>
  <div class="scroll-button animate-scroll">
    <a data-sveltekit-reload href="/about">More about me &#8594;</a>
  </div>
</div>

<style>
  .container {
    margin: 120px auto;
    max-width: 600px;
    min-width: 200px;
    text-align: center;
    display: block;
  }

  p {
    position: relative;
    letter-spacing: -0.03em;
    font-size: 1rem;
    line-height: 2rem;
    font-family: "Lucida Handwriting", "Courier New", monospace;
    margin: 0;
  }

  .scroll-button {
    margin-top: 5px;
    border: none;
    outline: none;
    cursor: pointer;
    font-weight: bold;
  }

  .profile-picture {
    float: left;
    margin-right: 40px;
    margin-left: 40px;
    width: 20%;
    max-width: 140px;
    min-width: 90px;
    height: auto;
    border-radius: 50%;
    border-collapse: separate;
  }
</style>
