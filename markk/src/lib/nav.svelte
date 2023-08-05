<script>
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  import { onMount } from "svelte";
  import logo from "$lib/assets/markk-logo.svg";

  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
  
  });
</script>

<header>
  <div class="header-wrapper">
      <nav>
    <img class="logo" src={logo} alt="">
        <ul>
              <li>
                  <a class="menu-item" href=" ">
                      <div class="hvr-circle"></div>
                      ons
                  </a>
              </li>
              <li>
                  <a class="menu-item" href=" ">
                      <div class="hvr-circle"></div>
                      werk
                  </a>
              </li>
              <li>
                  <a class="menu-item" href=" ">
                      <div class="hvr-circle"></div>
                      tactiek
                  </a>
              </li>
              <li>
                  <a class="menu-item" href=" ">
                      <div class="hvr-circle"></div>
                      blog
                  </a>
              </li>
              <li>
                  <a class="menu-item" href=" ">
                      <div class="hvr-circle"></div>
                      contact
                  </a>
              </li>
          </ul>
      </nav>
  </div>
</header>


<style>
  .header-wrapper {
    position: relative;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    height: 5em;
    width: 100%;
    padding: 2em;
}

.logo {
    width: 7em;
    cursor: pointer;
}

nav {
    position: relative;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    width: 100%;
}

.menu-item {
    text-decoration: none;
    color: var(--main-dark);
    cursor: pointer;
    transition: .2s;
    display: flex;
    flex-direction: row;
}

ul {
    display: flex;
    flex-direction: row;
    text-decoration: none;
    gap: 50px;
}

li {
    transition: .2s;
    list-style: none;
}

.hvr-circle {
    transform: scale(0);
    width: 10px;
    height: 10px;
    background-color: var(--main-dark);
    border-radius: 1em;
    margin-top: 7px;
    margin-right: 7px;
    transition: .3s;
}

.menu-item {
    font-size: 1em;
}

.menu-item:hover .hvr-circle {
    transform: scale(1);
}

.menu-item:active .hover-circle {
    transform: scale(1);
}
</style>
