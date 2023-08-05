<section>
  <div class="blog-intro">
    <div class="left">
      <h4>blog</h4>
      <p>
        Blogs, verhalen, onderzoekjes, bevindingen en ongezouten mening. Een
        maandelijks manifest vanuit eigen koker. Net als met voetbal, wiskunde
        of koken moet je met tekstschrijven en webdevelopment blijven oefenen en
        ontwikkelen om écht goed te worden. Dat doen we hier. Een kijkje in de
        breinen achter markk.
      </p>
      <p class="latest">latest -></p>
    </div>
    <div class="left-middle hover">
      <div class="overlay" />
      <img
        src="https://images.unsplash.com/photo-1551264950-49fb963d1493?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1287&q=80"
        alt=""
      />
    </div>
    <div class="right-middle hover">
      <div class="overlay" />
      <img
        src="https://images.unsplash.com/photo-1631558047913-b0ea074434a3?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1287&q=80"
        alt=""
      />
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
    max-width: 50%;
  }

  .left {
    position: relative;
    width: 33.3%;
    height: 100%;
    padding: 1em;
  }

  .latest {
    position: absolute;
    font-size: 2em;
    right: 0;
    bottom: 0;
  }

  .left-middle {
    width: 33.4%;
    height: 100%;
    overflow: hidden;
  }

  .right-middle {
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

  .overlay {
    position: absolute;
    background-color: var(--main-dark);
    height: 100%;
    width: 100%;
    opacity: 0;
    transition: 0.2s;
  }

  .hover:hover .overlay {
    opacity: 0.4;
    cursor: pointer;
  }
</style>
