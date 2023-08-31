<section>
  <div class="blog-intro">
    <div class="left">
      <!-- <h4>blog</h4> -->
      <p>
        Blogs, verhalen, onderzoekjes, bevindingen en ongezouten mening. Een
        maandelijks manifest vanuit eigen koker. Net als met voetbal, wiskunde
        of koken moet je met tekstschrijven en webdevelopment blijven oefenen en
        ontwikkelen om écht goed te worden. Dat doen we hier. Een kijkje in de
        breinen achter <span class="blue"> markk</span>.
      </p>
      <p class="latest"> ----></p>
      <div class="linehide"></div>
    </div>
    <div class="left-middle hover">
        <div class="lees blue">Lees blog</div>
        <div class="overlay2" />
        <div class="subscripts blue ">
            <div class="sub">de aftrap</div>
            <div class="date">05/08/2023</div>
        </div>
        <img
        src="https://images.unsplash.com/photo-1551264950-49fb963d1493?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1287&q=80"
        alt=""
        />
    </div>
    <div class="right-middle hover">
        <div class="lees white">Lees blog</div>
        <div class="overlay2" />
        <div class="subscripts white">
            <div class="sub">de sprint</div>
            <div class="date">05/08/2023</div>
        </div>
        <img
        src="https://images.unsplash.com/photo-1667906278742-306d3ad2e90b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1287&q=80"
        alt=""
        />
        <div class="linehide"></div>
    </div>
  </div>
</section>

<style>
  section {
    height: 80vh;
    width: 100%;
    padding: 0;
  }

  .blog-intro {
    position: relative;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: flex-end;
    height: max-content;
    width: 100%;
    height: 100%;
    overflow: hidden;
  }

  h4 {
    font-size: 7vw;
    font-weight: 600;
    margin-bottom: 5%;
    text-transform: uppercase;
  }

  p {
    max-width: 95%;
    font-size: 2.3vw;
    line-height: 1.1em;
  }

  .left {
    position: relative;
    width: 33.3%;
    height: 100%;
    padding: 1em;
  }

  .line {  
    position: absolute;
    width: 100%;
    border-top: solid 1px var(--main-dark);
    left: 0;
    bottom: 3em;
  }

  .latest {
    position: absolute;
    bottom: 2px;
    right: 0;
    font-size: 2em;
    padding: .3em;
    transition: .2s;
    z-index: 3;
  }

  .left-middle {
    position: relative;
    width: 33.4%;
    height: 100%;
    overflow: hidden;
  }

  .right-middle {
    position: relative;
    width: 33.3%;
    height: 100%;
    overflow: hidden;
  }

  img {
    object-fit: cover;
    height: 100%;
    width: 100%;
    padding: 0;
  }

  .overlay2 {
    position: absolute;
    background-color: var(--main-dark);
    height: 100%;
    width: 100%;
    opacity: 0;
    transition: 0.2s;
    z-index: 2;
  }

  .subscripts {
    position: absolute;
    bottom: 0em;
    width: 100%;
    display: flex;
    justify-content: space-between;
    font-size: 2em;
    padding: .3em;
    opacity: 0;
    transition: .2s;
    z-index: 3;
  }

  .hover:hover .subscripts {
    opacity: 1;
  }

  .sub {
  }

  .lees {
    position: absolute;
    top: .5em;
    font-size: 2em;
    left: .5em;
    opacity: 0;
    transition: .2s;
  }

  .date {
    font-size: .8em;
    transform: translateY(8px);
  }

  .hover:hover .overlay2 {
    opacity: 0.2;
    cursor: pointer;
  }

  .hover:hover .lees {
    opacity: 1;
  }

  .linehide {  
    position: absolute;
    width: 100%;
    border-top: solid 1px var(--main-dark);
    left: 0;
    bottom: 3em;
    opacity: 0;
  }


</style>
