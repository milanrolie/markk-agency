<script>
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  import { onMount } from "svelte";
  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
    gsap.to(".path-gsap", {
      fill: "#efefef",
      delay: 0,
      stagger: 0.1,
      duration: .7,
    });



    gsap.to(".overlay", {
      y: "-100%",
      delay: 2,
      stagger: 0.1,
      duration: .7,
      ease: "expo.easeOut",
    });

  

  });
</script>

<div class="overlay">
  <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
	 viewBox="0 0 354.8 104.4" style="enable-background:new 0 0 354.8 104.4;" xml:space="preserve">
<style type="text/css">
	.st0{fill:#7878F9;}
	.st1{fill:#EFEFEF;}
	.st2{fill:#4A54F5;}
	.st3{fill:#FFE7CE;}
</style>
<g>
	<path class="path-gsap" d="M0,104.4V34.5h22v69.9H0z"/>
	<path class="path-gsap" d="M45.1,104.4V34.5h22v69.9H45.1z"/>
	<path class="path-gsap" d="M169,104.4V85.6l3.3-17l-3.3-17V34.5h21.6v69.9H169z"/>
	<path class="path-gsap" d="M199.2,104.4V34.5h22v69.9H199.2z"/>
	<path class="path-gsap" d="M257.4,104.4V0h22v104.4H257.4z"/>
	<path class="path-gsap" d="M290.9,104.4V0h22v104.4H290.9z"/>
	<path class="path-gsap" d="M267.2,63.8l76.1-37.7l8.6,15.9l-78.2,39.7L267.2,63.8z"/>
	<path class="path-gsap" d="M201.7,52l43.7-17.6l9.3,15.4l-49.2,18.9L201.7,52z"/>
	<path class="path-gsap" d="M3,52l43.7-17.6l9.3,15.4L6.9,68.7L3,52z"/>
	<path class="path-gsap" d="M87.1,104.4V34.5h22v69.9H87.1z"/>
	<path class="path-gsap" d="M45.1,52l43.7-17.6l9.3,15.4L49,68.7L45.1,52z"/>
	<path class="path-gsap" d="M334.9,104.3L293,49.6l10.6-14.9l51.1,69.6H334.9z"/>
	<path class="path-gsap" d="M151.3,35.1c-19,0-34.4,15.4-34.4,34.4s15.4,34.4,34.4,34.4c19,0,34.4-15.4,34.4-34.4S170.3,35.1,151.3,35.1z M151.3,82.6
		c-7.3,0-13.1-5.9-13.1-13.1s5.9-13.1,13.1-13.1c7.3,0,13.1,5.9,13.1,13.1S158.6,82.6,151.3,82.6z"/>
</g>
</svg>

  <!-- <p><span class="percentage">0</span>%</p> -->
</div>

<style>
  .overlay {
    position: fixed;
    top: 0;
    height: 100svh;
    width: 100%;
    display: flex;
    align-items: flex-start;
    justify-content: flex-end;
    flex-direction: column;
    background-color: var(--main-dark);
    z-index: 100;
    /* border-radius: 3em; */
  }

  p {
    position: absolute;
    bottom: 5%;
    font-size: 1em;
}

svg {
    fill: var(--main-dark);
    height: 30%;
    transition: 0;
    overflow: visible;
  }

  @media screen and (max-width: 1122px) {
    svg {
      width: 30%;
    }
  }
</style>
