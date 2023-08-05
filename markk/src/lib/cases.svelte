<script>
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  import { onMount } from "svelte";

  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
    gsap.to(".case-wrapper", {
      scrollTrigger: {
        trigger: ".cases",
        scrub: 2,
        pin: true,
        start: "top+=120",
        end: "top+=1000",
      },
      x: "-55%",
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
      <img src="https://studiorolie.com/_app/immutable/assets/grrr-iphone.6eb41851.webp" alt="" />
      <h4>Family fitness</h4>
      <p>Website, Brand identity, Video</p>
    </div>
    <div class="case">
      <img
        src="https://studiorolie.com/_app/immutable/assets/favela.aba46be7.webp"
        alt=""
      />
      <h4>Family fitness</h4>
      <p>Website, Brand identity, Video</p>
    </div>
    <div class="case">
      <img
        src="https://images.unsplash.com/photo-1611532736597-de2d4265fba3?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=774&q=80"
        alt=""
      />
      <h4>Family fitness</h4>
      <p>Website, Brand identity, Video</p>
    </div>
    <div class="case">
      <img
        src="https://images.unsplash.com/photo-1611532736597-de2d4265fba3?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=774&q=80"
        alt=""
      />
      <h4>Family fitness</h4>
      <p>Website, Brand identity, Video</p>
    </div>
    <div class="case">
      <img
        src="https://images.unsplash.com/photo-1591258370814-01609b341790?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=774&q=80"
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
  h4 {
    font-size: 3em;
    font-weight: 300;
  }
  .cases {
    height: 120vh;
    width: 100%;
    /* overflow: hidden; */
    padding: 5%;
    padding-top: 10%;
  }

  .case-wrapper {
    position: relative;
    display: flex;
    flex-direction: row;
    gap: 1%;
    top: 10%;
    height: 90vh;
    width: max-content;
  }

  .case {
    width: 35vw;
    height: 70vh;
    clip-path: inset(0px);
    transition: 0.4s;
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

  .arrow {
    position: absolute;
    right: 5%;
    transform: translateY(-50px);
    fill: var(--main-bright);
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
</style>
