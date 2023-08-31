<script>
  import Nav from "$lib/Nav.svelte";
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  import { onMount } from "svelte";
  import Footer from "$lib/Footer.svelte";
  import Cases from "$lib/cases.svelte";
  import ink from "$lib/assets/legends-macbook2.jpg";
  import ink2 from "$lib/assets/legends-macbook.jpg";



  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
    gsap.to(".words", {
      y: 0,
      delay: 0.8,
      duration: 1.5,
      ease: "power4.out",
    });

    // gsap.to(".words", {
    //   scrollTrigger: {
    //     trigger: ".text-wrapper",
    //     scrub: 1,
    //     start: "top",
    //     end: "center",
    //     markers: true,
    //   },
    //   y: 0,
    // });

    gsap.to(".first-project-image", {
      scrollTrigger: {
        trigger: ".image",
        scrub: 1,
        start: "top-=200",
        end: "center+=200",
        // markers: true,
      },
      scale: 1.07,
    });

    gsap.from(".first-project-image", {
      y: 500,
      delay: 1,
      duration: 1.5,
      ease: "power4.out",
    });

    gsap.from(".date2", {
      y: 500,
      delay: 1.7,
      duration: 1.5,
      ease: "power4.out",
    });

    gsap.to(".second-project-image", {
      scrollTrigger: {
        trigger: ".second-project-image",
        scrub: 2,
        start: "top-=1200",
        end: "top-=200",
        stagger: 1,
        // markers: true,
      },
      y: 0,
      "--progress": 1,
    });

    gsap.to(".second-part2", {
      scrollTrigger: {
        trigger: ".second-part2",
        scrub: 2,
        start: "top-=1000",
        end: "top-=200",
        stagger: 1,
        // markers: true,
      },
      y: 0,
      "--progress": 1,
    });

    gsap.to(".third-project-image", {
      scrollTrigger: {
        trigger: ".third-project-image",
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
</script>

<Nav />

<section class="project-intro">
  <div class="text-wrapper">
    <h1 class="words">Ink football</h1>
    <p class="date2">23-10-2020</p>
  </div>
  <div class="image">
    <div class="img-clip">
      <img
        class="first-project-image"
        src={ ink2 }
        alt=" "
      />
    </div>
  </div>
  <div class="project-description">
    <div class="introduction">
      <p>
        Er was eens een jongeman die op reis ging naar Brazilië, daar verliefd
        werd op het land, en maar al te graag zijn steentje bij zou dragen om er
        voor iedereen een betere plek van te maken. Hij riep Ink in het leven.
        En zou de voetbalcultuur inzetten om kinderen in favelas een betere
        toekomst te geven.
      </p>
      <p>
        Daar helpen we hem maar al te graag bij vanuit onze expertise. Zoals bij
        ons meestal het geval, moest er een website komen. Waar bezoekers
        geïnspireerd worden om zich aan te melden als sponsor van het Ink
        talenten team. De droom: Ink als grootste club met impact van Brazilië.
      </p>
    </div>
    <div class="images">
      <img
        class="second-project-image project-clip-gsap"
        src= { ink }
        alt=""
      />
      <img
        class="second-project-image project-clip-gsap second-part2"
        src="https://www.mockupworld.co/wp-content/uploads/dynamic/2022/12/ipad-pro-m2-free-mockup-1072x0-c-default.jpg"
        alt=""
      />
    </div>
    <div class="introduction">
      <p>
        Het idee is dat je je als bezoeker echt sponsor voelt van het project.
        Niet simpelweg donateur, want dat is saai. En dat zijn wij niet. Je naam
        op de shirtjes, of sponsor het stadion. Spreekwoordelijk natuurlijk.
        Daarnaast moet de site Brazilië uitstralen en je moet je verbonden
        voelen met de talenten van Ink. 
      </p>
      <p>
        Dit hebben we gedaan door middel van
        FIFA-playercards, waarop de voetballers scores krijgen op basis van hun
        schoolresultaten. <br> <br>
        Beeld spreekt al gauw meer dan 1000 woorden, althans volgens mijn
        grafisch vormgevende compagnon, dus neus vooral even rond:
      </p>
    </div>
    <div class="images">
      <img
        class="third-project-image project-clip-gsap"
        src="https://images.unsplash.com/photo-1574281583557-6cd118037a4b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1480&q=80"
        alt=""
      />
    </div>
  </div>
</section>

<Cases />
<Footer />

<style>
  section {
    overflow-x: hidden;
  }

  .text-wrapper {
    position: sticky;
    top: 0;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    height: 40vh;
    padding: 2%;
    margin-bottom: 2%;
    z-index: -1;
  }

  h1 {
    color: var(--main-dark);
    font-size: 9vw;
    text-transform: none;
    line-height: 0.8em;
    font-weight: 600;
  }

  .words {
    transform: translateY(700px);
  }

  .date2 {
    position: absolute;
    right: 1%;
    font-weight: 400;
    padding: 0.5em 1em;
    color: var(--gunMetal);
    background-color: var(--dark);
  }

  .img-clip {
    height: 100%;
    width: 100%;
    overflow: hidden;
  }

  .project-clip-gsap {
    clip-path: inset(calc((1 - var(--progress)) * 100%) 0 0 0);
  }

  .image {
    position: relative;
    margin-bottom: -5px;
  }

  img {
    object-fit: cover;
    z-index: 2;
  }

  .first-project-image {
    width: 100%;
    height: 95vh;
  }

  .project-description {
    background-color: var(--gunMetal);
    padding-top: 7%;
  }

  .introduction {
    display: flex;
    flex-direction: row;
    gap: 5%;
    padding: 3% 20%;
    margin-bottom: 3%;
  }

  .introduction p {
    font-size: 1.2em;
    font-weight: 300;
    max-width: 40%;
  }

  .images {
    display: flex;
    flex-direction: row;
    gap: 2%;
    padding: 0% 20%;
    width: 100%;
  }

  .second-project-image {
    width: 50%;
    height: 75vh;
  }

  .third-project-image {
    width: 100%;
    height: 75vh;
    margin-bottom: 10%;
  }

  @media screen and (max-width: 1122px) {
    .text-wrapper {
      height: 30%;
      margin-top: 40%;
    }

    .introduction {
      flex-direction: column;
      padding: 5% 15%;
    }

    .introduction p {
      max-width: 90%;
      margin-bottom: 1em;
    }

    .images {
      display: flex;
      flex-direction: column;
      padding: 0% 10%;
    }

    .second-project-image {
      width: 100%;
      height: 50%;
      margin-bottom: 5%;
    }
  }

  @media screen and (max-width: 700px) {
    .first-project-image {
      width: 100%;
      height: 120%;
    }

    .images {
      padding: 0;
    }

    .date {
      font-size: 0.7em;
      display: none;
    }

    .introduction p {
      max-width: 100%;
      font-size: 1em;
    }
  }
</style>
