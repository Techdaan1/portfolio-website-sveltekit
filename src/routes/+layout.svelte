<script>
  let screenSize = 600;
  let isDropdownOpen = false;

  const handleDropdownClick = () => {
    isDropdownOpen = !isDropdownOpen;
  };
  const handleDropdownFocusLoss = ({ relatedTarget, currentTarget }) => {
    if (
      relatedTarget instanceof HTMLElement &&
      currentTarget.contains(relatedTarget)
    )
      return;
    isDropdownOpen = false;
  };
</script>

<svelte:window bind:innerWidth="{screenSize}" />
<nav>
  <div class="nav-container">
    <a href="/" title="Back to Homepage"
      ><img src="\dani.png" alt="logo" class="logo" /></a
    >
    {#if screenSize < 600}
      <ul style:visibility="{isDropdownOpen ? "visible" : "hidden"}">
        <li><a href="/" class="hamburger-link">Home</a></li>
        <li><a href="/about" class="hamburger-link">About</a></li>
        <li><a href="/projects" class="hamburger-link">My projects</a></li>
        <li><a href="/contact" class="hamburger-link">Contact</a></li>
      </ul>

      <div on:focusout="{handleDropdownFocusLoss}">
        <button class="button" on:click="{handleDropdownClick}">
          <div class="hamburger">
            <span class="bar"></span>
            <span class="bar"></span>
            <span class="bar"></span>
          </div>
        </button>
      </div>
    {:else if screenSize >= 600}
      <div class="nav-links">
        <a href="/" class="link">Home</a>
        <a href="/about" class="link">About</a>
        <a href="/projects" class="link">My projects</a>
        <a href="/contact" class="link">Contact</a>
      </div>
    {/if}
  </div>
</nav>

<div class="container">
  <!-- Pages will be injected below -->
  <slot />
</div>

<style>
  ul {
    margin-top: 15px;
    background-color: black;
    font-size: 12px;
    line-height: 1.7;
    padding: 130px 35px 20px 35px;
    transition: 0.7s ease;
    border-radius: 10px;
  }

  .button {
    background-color: black;
    border: none;
    margin: 0.25rem;
  }

  div.nav-container {
    max-height: 90px;
  }

  .nav-container {
    display: flex;
  }

  .logo {
    height: 80px;
    width: auto;
  }

  .hamburger-link {
    font-family: "Lucida Handwriting", "Courier New", monospace;
    flex-shrink: 2;
    color: goldenrod;
  }

  .link {
    font-family: "Lucida Handwriting", "Courier New", monospace;
    flex-shrink: 2;
    transition: 0.7s ease;
    color: goldenrod;
  }

  .link:hover {
    color: cornsilk;
  }

  .hamburger {
    display: none;
    cursor: pointer;
  }
  .bar {
    display: block;
    width: 50px;
    height: 4px;
    margin: 8px auto;
    margin-right: 10px;
    -webkit-transition: all 0.3s ease-in-out;
    transition: all 0.3s ease-in-out;
    background-color: goldenrod;
  }

  @media (max-width: 600px) {
    .hamburger {
      display: block;
    }

    .hamburger.active .bar:nth-child(2) {
      opacity: 0;
    }
    .hamburger.active .bar:nth-child(1) {
      transform: translateY(8px) rotate(45deg);
    }
    .hamburger.active .bar:nth-child(3) {
      transform: translateY(-8px) rotate(-45deg);
    }
    .nav-links {
      position: fixed;
      left: -100%;
      top: 70px;
      gap: 0;
      flex-direction: column;
      background-color: black;
      width: 100%;
      text-align: center;
      transition: o.3s;
    }
    .link {
      margin: 16px 0;
    }
    .nav-links:active {
      left: 0;
    }
  }
</style>
