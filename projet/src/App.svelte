<script>
  //Importing router from svelte
  import Router from "svelte-spa-router";
  //Importing components
  import Home from "./lib/homepage/Home.svelte";
  import Error404 from "./lib/error404/Error404.svelte";
  import Adding_riddle from "./lib/adding_riddle/Adding_riddle.svelte";
  import About_us from "./lib/about_us/About_us.svelte";
  import Connection from "./lib/connection/Connection.svelte";
  import Subscription from "./lib/subscription/Subscription.svelte";
  import Defined_theme_riddle from "./lib/defined_theme_riddle/Defined_theme_riddle.svelte";
  import Scores from "./lib/scores/Scores.svelte";
  import Random_game from "./lib/random_game/Random_game.svelte";
  import Contact from "./lib/contact/Contact.svelte";
  
    const routes = {
      '/': Home,
      '/add_a_riddle': Adding_riddle,
      '/about_us': About_us,
      '/connection': Connection, 
      '/subscription': Subscription,
      '/defined_theme_riddle/': Defined_theme_riddle,
      '/defined_theme_riddle/:themeId': Defined_theme_riddle,
      '/scores': Scores,
      '/scores/:themeId': Scores,
      '/random_theme_riddle': Random_game,
      '/contact': Contact,
  
      //If no matching route found, then we redirect to Error page
      '*': Error404
    }
  </script>
  
  <body>
    <Router {routes} />
  </body>