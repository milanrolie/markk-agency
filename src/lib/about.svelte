<script>
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  import { onMount } from "svelte";

  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
    const projects = [".img2", ".img3"];
    projects.forEach((project) => {
      gsap.to(project, {
        scrollTrigger: {
          trigger: project,
          scrub: 2,
          start: "top-=1200",
          end: "top-=200",
          stagger: 1,
          // markers: true,
        },
        y: 0,
        "--progress": 1,
      });
    });

    gsap.from(".bg-color", {
      scrollTrigger: {
        trigger: ".about",
        scrub: 2,
        start: "top-=1000",
        end: "top-=300",
        // markers: true,
      },
      y: 200,
    });

    gsap.to(".lineword", {
      scrollTrigger: {
        trigger: ".about",
        scrub: 2,
        start: "top-=300",
        end: "top-=100",
        // markers: true,
      },
      y: 0,
   
    });
  });
</script>

<section class="about">
  <div class="bg-color" />
  <div class="about-container">
    <div class="ons"> --- </div>
    <h3>
      <div class="inline-block">
      <span class="lineword line1">van samen</span>
      </div>
      <div class="inline-block">
      <span class="lineword line2"> scoren naar samen </span>
      </div>
      <div class="inline-block">
      <span class="lineword line3"> websites maken</span>
      </div>
    </h3>
    <p class="about-text">
      Wij zijn <span class="blue">markk</span>, twee spontane jongens uit het
      noorden van het westen van het land. Als er iets is waar onze hartjes
      sneller van gaan kloppen is het mooie en rete goed werkende websites
      maken, waar andermans hartjes dan weer sneller van gaan kloppen. Wij
      helpen je jouw verhaal vertellen, via web -strategie, -design en
      -development. Dit doen we 100% op maat in custom code of we bouwen in
      WordPress. Allemaal zodat zowel Google als jouw doelgroep er helemaal
      gelukkig van worden. Onderscheidend en altijd met ballen.
    </p>
    <!-- <p>est. 2022</p> -->
    <div class="old-image-wrapper">
      <img
      class="img2"
      src="https://images.unsplash.com/photo-1622659097509-4d56de14539e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1287&q=80"
      alt=""
      />
      <img
      class="img3"
      src="https://images.unsplash.com/photo-1563433792993-4721561154b1?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1335&q=80"
      alt=""
      />
      <div class="date">
        <p>24-2-2020</p>
        <p>----------------------------------------------------------------------</p>
        <p>24-2-2020</p>
      </div>
    </div>
  </div>

  <!-- <div class="line" /> -->
</section>

<style>
  section {
    position: sticky;
    top: 0;
  }

  .about {
    height: 120vh;
    margin-top: -3%;
    /* background-color: #FE654F; */
    color: var(--main-offwhite);
  }
  
  .bg-color {
    position: relative;
    position: absolute;
    top: 0;
    left: 0;
    height: 100%;
    width: 100%;
    z-index: -1;
    transform: translateY(-50px);
  }

  .ons {
    position: absolute;
    top: 1em;
    right: 1em;
    color: black;
    transform: translateY(-50px);
    font-size: 2em;
  }
  
  .about h3 {
    font-size: 11vw;
    max-width: 100vw;
    font-weight: 500;
    line-height: 0.9em;
    z-index: 2;
    transform: translateY(-50px);
    color: var(--main-dark);
  }
  
  .lineword {
    display: inline-block;
    transform: translateY(-200px);
  }
  
  .inline-block {
    clip-path: polygon(0 0, 220% 0, 220% 100%, 0% 100%);
  }

  .about-text {
    max-width: 35%;
    font-size: clamp(1em, 1.2em, 3rem);
    margin-top: 2%;
    color: var(--main-dark);

  }

  .line {
    position: absolute;
    bottom: 5em;
    border-top: 2px solid var(--main-dark);
    width: 96%;
  }

  .old-image-wrapper {
    position: absolute;
    display: flex;
    flex-direction: row;
    gap: 2%;
    bottom: 1em;
    right: 2%;
    align-items: flex-end;
  }

  img {
    object-fit: cover;
    filter: grayscale(1);
    width: 25vw;
    clip-path: inset(calc((1 - var(--progress)) * 100%) 0 0 0);
  }

  .img1 {
    height: 13vw;
  }
  
  .img2 {
    position: relative;
    height: 25vw;
  }
  
  .img3 {
    position: relative;
    height: 35vw;
  }

  .date {
    position: absolute;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    bottom: -2em;
    right: 0;
    color: var(--main-dark);
    width: 100%;
  }
</style>
