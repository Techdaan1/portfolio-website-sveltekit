<script>
  export let name = "";
  export let info = "";
  export let src = "";
  export let alt = "";
  export let githubrepo = "";
  export let livedemo = "";
</script>

<div class="project-container">
  <div class="project-item" style="border-radius: 25px">
    <h2>{name}</h2>
    <div class="project-image">
      <img src="{src}" alt="{alt}" />
    </div>
    <div class="project-info">
      <p>{info}</p>
    </div>
    <div class="project-links">
      <a class="github-link" href="{githubrepo}">Github repo</a>
      {#if livedemo}
        <a class="demo-link" href="{livedemo}">Live demo</a>
      {/if}
    </div>
  </div>
</div>

<style>
  h2 {
    text-align: center;
    margin: 15px 0 0 0;
  }
  p {
    font-size: 12px;
  }

  .project-container {
    justify-content: center;
    display: inline-block;
    margin: 10px 10px;
  }

  .project-item {
    background-color: #e6e6e6;
    min-height: 400px;
    border-radius: 25px;
    display: flex;
    justify-content: space-between;
    flex-direction: column;
  }

  .project-info {
    margin-left: 20px;
    margin-right: 20px;
  }

  .project-links {
    background-color: darkgoldenrod;
    display: flex;
    border-radius: 10px;
  }

  .project-image {
    display: flex;
    justify-content: space-evenly;
  }

  div > img {
    max-width: 300px;
    max-height: 170px;
  }

  .github-link,
  .demo-link {
    background-color: black;
    color: white;
    padding: 4px 4px;
    margin: 10px;
    text-decoration: none;
    flex-basis: 50px;
    flex-grow: 1;
    flex-shrink: 1;
    text-align: center;
  }
</style>
