<script>
  export let name = "";
  export let info = "";
  export let src = "";
  export let alt = "";
  export let githubrepo = "";
  export let livedemo = "";
</script>

<div class="project-item">
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

<style>
  .project-item {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    background-color: #e6e6e6;
    padding: 10px;
    border-radius: 25px;
    height: 100%;
  }

  h2 {
    text-align: center;
    margin: 15px 0;
  }

  .project-image {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .project-image img {
    max-width: 100%;
    max-height: 170px;
    border-radius: 10px;
  }

  .project-info {
    font-size: 12px;
    margin: 10px 0;
  }

  .project-links {
    background-color: darkgoldenrod;
    display: flex;
    border-radius: 10px;
    margin-top: auto;
  }

  .github-link,
  .demo-link {
    background-color: black;
    color: white;
    padding: 4px;
    margin: 10px;
    text-decoration: none;
    flex: 1;
    text-align: center;
    border-radius: 5px;
  }
</style>
