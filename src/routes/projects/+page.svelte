<script>
  import Project from "../../Project.svelte";
</script>

<svelte:head>
  <title>Projects</title>
</svelte:head>

<div class="project-container">
  <div class="project-item">
    <Project
      name="Portfolio website"
      info="This is a responsive website to show my professional portfolio. It is
built with Sveltekit, HTML and CSS."
      src="/screenshot portfolio.png"
      alt="Screenshot portfolio"
      githubrepo="https://github.com/Techdaan1/portfolio-website-svelte"
    />
  </div>
  <div class="project-item">
    <Project
      name="To do list app"
      info="This is a basic to-do-list app to practice with the Vue.js
framework. A user can add and delete todos, edit them and mark
them as completed."
      src="/screenshot to do list app.png"
      alt="Screenshot To do list app"
      githubrepo="https://github.com/Techdaan1/to-do-list-app"
      livedemo="https://techdaan1.github.io/to-do-list-app/"
    />
  </div>
  <div class="project-item">
    <Project
      name="Pokedéx app"
      info="This is a simple Pokédex application built with Javascript,
HTML, CSS, and Bootstrap. Users can search through a collection
of Pokémon that is loading from an external source(API). Images
and information about the specific Pokémon can be displayed in a
modal by clicking on a Pokémons name."
      src="/screenshot pokedex.png"
      alt="Screenshot Pokedéx"
      githubrepo="https://github.com/Techdaan1/my-first-js-app"
      livedemo="https://techdaan1.github.io/my-first-js-app/"
    />
  </div>
  <div class="project-item">
    <Project
      name="MyFlix client - React"
      info="This is the client-side of a movie database app called myFlix
which fetches data from its server-side(API). It provides users
with information about different movies, directors, and genres.
Users will also be able to register, update their personal
information, and create a list of their favorite movies. It's
built using the MERN stack"
      src="/screenshot myflix.png"
      alt="Screenshot MyFlix client - React"
      githubrepo="https://github.com/Techdaan1/myFlix-client"
      livedemo="https://watch-myflix.netlify.app/"
    />
  </div>
  <div class="project-item">
    <Project
      name="MyFlix backend (API)"
      info="This is the backend (server side) of myFlix, a movie database
app in which users can search for and save information about
movies. It is developed using Node.js, Express and Mongoose. The
web app will provide users with information about different
movies, directors, and genres. It's built using the MERN stack."
      githubrepo="https://github.com/Techdaan1/movie_api"
    />
  </div>
  <div class="project-item">
    <Project
      name="Meet app"
      info="This is a serverless, progressive web app (PWA) built with React
using a test-driven development (TDD) technique. The app uses
the Google Calendar API to fetch upcoming events for the
selected city. It uses AWS Lambda as the authorization server. A
service worker allows the app to work offline. The Recharts
library is used to visualize data with a scatter graph and a pie
chart."
      src="screenshot meet app.png"
      alt="Screenshot Meet app"
      githubrepo="https://github.com/Techdaan1/meetup-app"
      livedemo="https://techdaan1.github.io/meetup-app/"
    />
  </div>
  <div class="project-item">
    <Project
      name="Native Chat app"
      info="This is a mobile chat app built with Gifted Chat that allows
users to chat with each other. The users can pick a background
color, read and send messages, share images and their location.
The app uses React Native Async Storage to allow users to view
stored messages when offline. Firestore has been used to store
data."
      src="screenshot chat app.jpg"
      alt="Screenshot Native Chat app"
      githubrepo="https://github.com/Techdaan1/chat"
    />
  </div>
  <div class="project-item">
    <Project
      name="MyFlix client - Angular"
      info="This myFlix movie app has been created using Angular. MyFlix is
allowing users to create a profile, log in and see a list of
movies. But also gives you the option to see the genre, director
and single movie description. Your favorite movies you can add
to a favorite movies list. The app has been built using Angular,
Angular Material and Typescript and works with the myFlix API."
      src="screenshot angular myflix.png"
      alt="Screenshot MyFlix client - Angular"
      githubrepo="https://github.com/Techdaan1/angular-client-myflix"
      livedemo="https://techdaan1.github.io/angular-client-myflix/"
    />
  </div>
  <div class="project-item">
    <Project
      name="ComfyHouse app"
      info="This is a responsive website thats shows a small webshop. It is
built with Javascript and CSS."
      src="/screenshot comfyhouse.png"
      alt="Screenshot ComfyHouse"
      githubrepo="https://github.com/Techdaan1/javascript-store"
      livedemo="https://javascript-store-practice.netlify.app/"
    />
  </div>
</div>

<style>
  .project-container {
    display: grid;
    justify-content: center;
    display: -ms-grid;
    -ms-grid-columns: 1fr 1fr;
    grid-template-columns: 1fr 1fr 1fr;
    display: inline-block;
    margin: 10px;
  }

  .project-item {
    margin: 5px;
  }

  @supports (display: grid) {
    .project-container {
      display: -ms-grid;
      display: grid;
      -ms-grid-columns: 1fr 1fr 1fr;
      grid-template-columns: 1fr 1fr 1fr;
    }
  }

  @media all and (max-width: 550px) {
    .project-container {
      grid-template-columns: 1fr;
    }
  }

  @media all and (min-width: 550px) and (max-width: 850px) {
    .project-container {
      grid-template-columns: 1fr 1fr;
    }
  }

  @media all and (max-width: 850px) {
    .project-container {
      grid-gap: 10px;
    }

    .project-item:last-child {
      -ms-grid-column: auto / auto;
      grid-column: auto / auto;
      -ms-grid-row: auto / auto;
      grid-row: auto / auto;
    }
  }
</style>
