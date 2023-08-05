<script>
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  import { onMount } from "svelte";

  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
    gsap.to(".word", {
      y: 0,
      stagger: 0.2,
      delay: 0.2,
      duration: 0.1,
    });

    gsap.to(".intro", {
      y: 0,
      delay: 1,
      duration: 2,
    //   ease: "power4.out",
    });

    gsap.to(".creatief", {
      scrollTrigger: {
        trigger: ".home",
        scrub: 1,
        start: "top",
        end: "top+=200",
      },
      x: -100,
      duration: 1,
    //   ease: Power2.easeinOut,
    });

    gsap.to(".webbureau", {
      scrollTrigger: {
        trigger: ".home",
        scrub: 1,
        start: "top",
        end: "top+=200",
      },
      x: 50,
      stagger: 0.5,
      duration: 1,
    //   ease: Power2.easeinOut,
    });

    gsap.to(".ballen", {
      scrollTrigger: {
        trigger: ".home",
        scrub: 1,
        start: "top",
        end: "top+=200",
      },
      x: -50,
      stagger: 0.5,
      duration: 1,
    //   ease: Power2.easeinOut,
    });

    gsap.to(".intro", {
      scrollTrigger: {
        trigger: ".home",
        scrub: 1,
        start: "top",
        end: "top+=200",
      },
      x: 150,
      duration: 1,
    //   ease: Power2.easeinOut,
    });

    gsap.to(".ball", {
      scrollTrigger: {
        trigger: ".home",
        scrub: 1,
        start: "top",
        end: "top+=200",
      },
      scale: 0,
      stagger: 0.5,
      duration: 1,
    //   ease: Power2.easeinOut,
    });

    gsap.to(".home", {
      scrollTrigger: {
        trigger: ".home",
        scrub: 1,
        start: "top",
        end: "top+=200",
      },
      y: -300,
      stagger: 0.5,
      duration: 1,
    //   ease: Power2.easeinOut,
    });
  });
</script>

<div class="title-wrapper">
  <section class="home">
    <div class="title-wrapper">
      <h1>
        <span class="creatief word">creatief</span>
        <span class="webbureau word">webbureau</span> <br />
        <span class="met word">met</span>
        <span class="ballen word"> ballen</span>
      </h1>
      <div class="ball" />
      <div class="intro-animation">
        <h2 class="intro">webdesign op champions league niveau, want dat hebben wij voetballend nooit gehaald.</h2>
      </div>
    </div>
  </section>
</div>

<style>
  .home {
    position: relative;
    height: 88vh;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  h1 {
    font-size: 13vw;
    font-weight: 300;
    line-height: 0.9em;
    text-align: center;
  }

  h2 {
    position: absolute;
    font-size: 1.3em;
    font-weight: 200;
    max-width: 20%;
    left: 60%;
  }

  .creatief {
    margin-right: 40%;
    clip-path: polygon(0 0, 100% 0, 100% 100%, 0% 100%);
  }

  .webbureau {
    margin-left: 20%;
    clip-path: polygon(0 0, 100% 0, 100% 100%, 0% 100%);
  }

  .ballen {
    margin-left: 0;
    clip-path: polygon(0 0, 100% 0, 100% 100%, 0% 100%);
  }

  .met {
    color: var(--main-bright);
    font-style: oblique;
    margin-left: -10%;
  }

  .word {
    transform: translateY(-500px);
    transition: transform 0.5s;
  }

  .ball {
    position: absolute;
    border-radius: 100%;
    left: 53%;
    background-color: var(--main-bright);
    height: 10vh;
    width: 10vh;
  }

  .intro-animation {
    clip-path: polygon(0 0, 100% 0, 100% 100%, 0% 100%);
    height: 150px;
    transform: translateY(0px);
  }

  .intro {
    /* transform: translateY(-100px); */
  }
</style>
