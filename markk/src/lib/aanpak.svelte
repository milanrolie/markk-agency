<script>
    import { gsap } from "gsap";
    import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
    import { onMount } from "svelte";
  
    gsap.registerPlugin(ScrollTrigger);
  
    onMount(() => {
    gsap.to(".numb", {
      opacity: 1,
      duration: .0001,
      scrollTrigger: {
        trigger: ".aanpak",
        start: "top bottom",
        end: "bottom+=200 bottom",
        toggleActions: "play reverse play reverse",
      },
    });

      gsap.to(".number", {
        scrollTrigger: {
          trigger: ".aanpak",
          scrub: 0,
          start: "top center",
          end: "bottom bottom",
        },
        innerText: 100,
        snap: {
        innerText: 1,
      },
    });
  
    });
  </script>












<section class="aanpak">
  <div class="section-wrapper">
    <div class="left-side">
      <div class="numb"> <span class="number">0</span>% </div>
    </div>

    <div class="right-side">
      <h3>tactiek</h3>
      <p>Scoren doe je samen, wij geven de voorzet, jij kopt hem in. Samen scoren met ons ziet er vaak als volgt uit:</p>
      <ul>
        <li>
            <p class="label">1. Koffie drinken</p>
          <p>
            Omdat alle goede samenwerkingen beginnen met koffie. (Thee is
            natuurlijk ook goed)
          </p>
        </li>
        <li>
          <p class="label">2. Jouw verhaal in kaart</p>
          <p>
            Het verhaal van jouw onderneming retegoed begrijpen is misschien wel
            de allerbelangrijkste stap in ons proces.
          </p>
        </li>
        <li>
          <p class="label">3. Concept & Strategie</p>
          <p>
            Vervolgens gaan wij de creatieve motor eens flink aanzetten om een
            concept en strategie te bedenken.
          </p>
        </li>
        <li>
          <p class="label">4. Schets</p>
          <p>
            Hier rolt een schets uit waarin we kijken naar opbouw en structuur
            van de site. En als deze is goedgekeurd…
          </p>
        </li>
        <li>
          <p class="label">5. Content</p>
          <p>
            Content vormt de <i>ziel</i> van je site. Tijd om je verhaal te vertellen
            met tekst, foto, video en animatie.
          </p>
        </li>
        <li>
          <p class="label">6. Bouwen</p>
          Nu begint het echte werk en gaan we de site voor het eggie bouwen. Laag
          voor laag, pagina voor pagina.
          <p />
        </li>
        <li>
          <p class="label">7. Feedback & Testen</p>
          <p>
            Tijd voor de puntjes op de ï, en testen tot we een ons wegen. Werkt
            alles zoals het hoort?
          </p>
        </li>
        <li>
          <p class="label">8. Scoren maar!</p>
          <p>
            Dan kop jij hem in en is het tijd om te scoren met je gloednieuwe
            online identiteit!
          </p>
        </li>
    </ul>
    <p class="andere-taktiek">
        Uiteraard is iedere aanval anders, soms vraagt het om een aanpak over de
        flanken, soms juist recht door het midden. Tactiek bespreken we altijd
        samen voor de wedstrijd.
      </p>
    </div>
</div>
</section>

<style>
  .aanpak {
    height: auto;
    width: 100%;
    background-color: var(--main-dark);
    color: var(--main-offwhite);
    padding: 0;
}

.section-wrapper {
    position: relative;
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: row;
    padding: 5em 1em;
  }

  .left-side {
    width: 17.5%;
    height: 100%;
  }

  .numb {
    position: fixed;
    bottom: 0;
    font-weight: 300;
    opacity: 0;
    font-size: 6vw;

  }

  .right-side {
    width: 82.5%;
  }

  h3 {
    font-size: 10vw;
  }

  ul {
  }

  li {
    list-style-type: none;
    font-size: 3vw;
    padding: 2rem 0;
    border-top: 2px solid var(--main-offwhite);
  }

  li p {
    font-size: 1em;
  }


.label {
    margin-bottom: 2%;
    width: max-content;
    text-transform: lowercase;
    border: 1px solid var(--main-offwhite);
    width: max-content;
    padding: 6px 15px;
    border-radius: .2em;
    margin-bottom: 1em;
    font-size: 1.2rem;

  }

  .andere-taktiek {
    font-size: 3rem;
    width: 100%;
    font-weight: 600;
    margin-top: 10%;
  }
</style>
