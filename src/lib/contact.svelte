<script>
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  import { onMount } from "svelte";

  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
    gsap.to(".image ", {
      scrollTrigger: {
        trigger: ".image",
        scrub: 1,
        start: "top",
        end: "center",
        pin: ".image",
      },
    });

    gsap.to(".image-overlay", {
      scrollTrigger: {
        trigger: ".image",
        scrub: 1,
        start: "top",
        end: "center",
        pin: ".image-overlay",
      },
      opacity: 1,
    });

    gsap.to(".photo-title", {
      scrollTrigger: {
        trigger: ".image",
        scrub: 1,
        start: "top",
        end: "center",
        pin: ".clip",

      },
      y: -100,
    });
    
  });
</script>

<section class="contact">
  <div class="photography">
      <div class="image-overlay" />
    <img class="image"
      src="https://images.unsplash.com/photo-1634287585403-2d287599063a?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=3180&q=80"
      alt=""
    />
    <div class="clip"> 
      <h2 class="photo-title">speelboek</h2>
    </div>
</section>

<style>
  .contact {
    /* position: sticky; */
    top: 0px;
    width: 100%;
    padding: 0;
    margin-bottom: 0%;
    height: auto;
  }
  
  .photography {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  img {
    position: relative;
    height: 70vh;
    width: 100%;
    object-fit: cover;
    z-index: 1;
  }
  
  .image-overlay {
    position: absolute;
    height: 100%;
    width: 100%;
    background-color: var(--dark);
    z-index: 2;
    opacity: 1;    
  }

  .clip {
    display: flex;
    align-items: center;
    justify-content: center;
    position: absolute;
    height: 500px;
    width: 100%;
    z-index: 5;
    clip-path: inset(0 0 40% 0);   
    /* background-color: aqua;  */
    
  }
  
  h2 {
    position: absolute;
    top: 20%;
    font-size: 10vw;
    line-height: .8em;
    font-weight: 600;
    text-align: center;
    text-transform: lowercase;
    transform: translateY(200px);
    color: var(--main-offwhite);
    z-index: 3;
  }
  
</style>
