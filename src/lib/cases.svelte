<script>
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  import { onMount } from "svelte";
  import ink from "$lib/assets/legends-macbook2.jpg";

  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
    gsap.to(".case-wrapper", {
      scrollTrigger: {
        trigger: ".cases",
        scrub: 4,
        // pin: true,
        start: "top+=100",
        end: "bottom",
        // markers:true,
      },
      x: "-50%",
    });
    const circle = document.getElementById("circle");
    const cursorText = document.querySelector(".cursor-text");
    const circleStyle = circle.style;

    document.addEventListener("mousemove", (e) => {
      window.requestAnimationFrame(() => {
        if (
          e.target.classList.contains("case") ||
          e.target.closest(".case-wrapper")
        ) {
          // circle.classList.add('biggercircle')
          cursorText.innerHTML = "BEKIJK <br> PROJECT";
        } else {
          // circle.classList.remove('biggercircle')
        }

        circleStyle.top = `${e.clientY}px`;
        circleStyle.left = `${e.clientX}px`;
      });
    });
  });
</script>

<section class="cases">
  <h4>Zie hoe ons werk voor anderen werkt.</h4>
  <div class="case-wrapper">
    <div class="case">
      <img
        src="https://studiorolie.com/_app/immutable/assets/grrr-iphone.6eb41851.webp"
        alt=""
      />
      <h4>Family fitness</h4>
      <p>Website, Brand identity, Video</p>
    </div>
    <div class="case">
      <img src={ink} alt="" />
      <h4>Family fitness</h4>
      <p>Website, Brand identity, Video</p>
    </div>
    <a href="/ink">
      <div class="case">
        <img
          src="https://images.unsplash.com/photo-1590771998996-8589ec9b5ac6?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1287&q=80"
          alt=""
        />
        <h4>Family fitness</h4>
        <p>Website, Brand identity, Video</p>
      </div>
    </a>
    <div class="case">
      <img
        src="https://twintig-utrecht.nl/wp-content/uploads/2022/01/Ruimte.png"
        alt=""
      />
      <h4>Family fitness</h4>
      <p>Website, Brand identity, Video</p>
    </div>
    <div class="case bluebg" />
    <div class="case">
        <img
          src="https://images.unsplash.com/photo-1590771998996-8589ec9b5ac6?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1287&q=80"
          alt=""
        />
        <h4>Family fitness</h4>
        <p>Website, Brand identity, Video</p>
      </div>
  </div>
  
  <div id="circle" class="circle">
    <p class="cursor-text" />
    <div class="line" />
  </div>
</section>

<style>
  section {
    padding-left: 0%;
  }

  h4 {
    font-size: 4vw;
    font-weight: 700;
    margin-bottom: 3%;
    color: var(--main-bright);
  }
  .cases {
    height: 100vh;
    width: 100%;
    /* padding: 2%; */
    padding-bottom: 0;
    padding-top: 30vh;
    margin-bottom: 13vh;
  }

  .case-wrapper {
    position: relative;
    display: flex;
    flex-direction: row;
    /* gap: 1%; */
    width: max-content;
    height: 100%;
  }

  .case {
    width: 35vw;
    height: 100%;
    clip-path: inset(0px);
    transition: 0.4s;
    cursor: pointer;
  }

  .case:hover {
    clip-path: inset(10px);
  }

  .case img {
    width: 100%;
    height: 100%;
    transition: 0.4s;
    object-fit: cover;
    margin-bottom: 4%;
  }

  .case img:hover {
    transform: scale(1.03);
  }

  .circle {
    position: fixed;
    width: 50px;
    height: 50px;
    background-color: var(--main-accent);
    border-radius: 50%;
    transition: ease-out 0.2s, transform ease-in 0.2s;
    z-index: 10000;
    opacity: 0;
    pointer-events: none;
    font-size: 0.9em;
  }

  .cursor-text {
    transform: translatey(120%) translateX(2px);
    font-family: "urbanist", sans-serif;
    font-size: 0.6em;
    line-height: 0.9em;
    mix-blend-mode: normal;
    transition: 1s;
  }

  .case-wrapper:hover .circle {
    opacity: 1;
    transform: scale(2);
  }

  .bluebg {
    background-color: var(--main-dark);
  }
</style>
