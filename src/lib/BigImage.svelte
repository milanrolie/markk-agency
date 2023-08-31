<script>
    import { gsap } from "gsap";
    import { ScrollTrigger } from "gsap/dist/ScrollTrigger"
 	import { onMount } from "svelte";

    gsap.registerPlugin(ScrollTrigger)



onMount(() => {
    gsap.to(".big-image", {
    scrollTrigger: {
        trigger: '.big-image',
        scrub: 1,
        start: 'top-=700',
        end: 'top+=300',
    },
    y: -100,
    '--progress': 1
});
});


</script>

<section>
<img class="big-image" src="https://images.unsplash.com/photo-1497699238310-892cfa1fedb7?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=3371&q=80" alt="">
</section>

<style>
    section{
        display: flex;
        align-items: center;
        justify-content: center;
        padding: 0;
    }

    img {
        object-fit: cover;
        height: 70vh;
        width: 110%;
        clip-path: inset(0 calc((1 - var(--progress)) * 20%) 0 calc((1 - var(--progress)) * 20%));
    }

    @media screen and (max-width: 1122px) {
    section {
        display: none;
    }
  }
</style>
