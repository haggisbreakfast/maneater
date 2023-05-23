<template>
  <img alt="maneater band" class="photo drop-shadow" src="./assets/maneater.jpg" />
  <img alt="maneater" src="./assets/maneater-type.png" class="banner"/>
  <img alt="drawing of a person eating spaghetti" src="./assets/maneater-man.png" class="background-person" style="left: 4rem; top: 2rem;"/>
  <img alt="drawing of a person eating spaghetti" src="./assets/maneater-man.png" class="background-person" style="right: 8rem; top: 10rem;"/>
  <img alt="drawing of a person eating spaghetti" src="./assets/maneater-man.png" class="background-person" style="right: 4rem; top: 6rem;"/>
  <img alt="drawing of a person eating spaghetti" src="./assets/maneater-man.png" class="background-person" style="right: 9rem; top: 17rem;"/>
  <img alt="drawing of a person eating spaghetti" src="./assets/maneater-man.png" class="background-person" style="left: 60rem; top: 40rem;"/>
  <img alt="drawing of a person eating spaghetti" src="./assets/maneater-man.png" class="background-person" style="left: 2rem; top: 45rem;"/>
  <img alt="drawing of a person eating spaghetti" src="./assets/maneater-man.png" class="background-person" style="left: 10rem; bottom: 10rem;"/>
  <img alt="drawing of a person eating spaghetti" src="./assets/maneater-man.png" class="background-person" style="left: 3rem; top: 26rem;"/>  
  <ul class="socials">
    <li>
      <a href="https://maneaterband.bandcamp.com/">
        <img src="./assets/bandcamp.svg" />
      </a>
    </li>
    <li>
      <a href="https://open.spotify.com/artist/1KCkpddjYD7xdWSVZMmxgc?si=6IofNe5aTv6m5nJoI8pkog">
        <img src="./assets/spotify.svg" />
      </a>
    </li>
    <li>
      <a href="https://twitter.com/maneaterband">
        <img src="./assets/twitter.svg" />
      </a>
    </li>
    <li>
      <a href="https://www.instagram.com/maneaterband/">
        <img src="./assets/instagram.svg" />
      </a>
    </li>
    <li>
      <a href="https://www.facebook.com/maneaterband">
        <img src="./assets/facebook.svg" />
      </a>
    </li>
  </ul>
  <div class="content-window-container">
    <ContentWindow title="past shows" :list="[{name: 'Sled Island Festival', link:'https://www.sledisland.com/2019/maneater', venue: 'Calgary, AB'}, 
    {name: 'Arts Assembly Annual Fundraiser', link: 'https://www.artsassembly.ca/act-3', venue: 'Red Gate - Vancouver, BC'}, 
    {name: 'Copper Owl', link: 'https://www.artsassembly.ca/act-3', venue: 'Victoria, BC'}, {name: 'Victory Lounge', link: 'https://www.artsassembly.ca/act-3', venue: 'Seattle, WA'}, {name: 'Greenhouse', link: 'https://www.artsassembly.ca/act-3', venue: 'Portland, OR'} ]"/>
    <ContentWindow title="press" :list="[{name: 'Stereogum', link: 'https://www.stereogum.com/1946986/maneater-noise/premiere/?fbclid=IwAR1zsjmt7-vbIMfdM3GJ4Vxz_M1iWrknbBpt3vKpOIjse1TCnnCDd2mMyTg'}, {name: 'Gold Flake Paint', link: 'https://www.goldflakepaint.co.uk/review-maneater-maneater/?fbclid=IwAR3VNXm2dLlmMmI1gydNCg-GnN7cWAT0w04IpbUNthlpMV3J8P8851uvIZM'}, { name:'CiTR Radio live set & interview', link:'https://www.citr.ca/radio/noise-complaint/episode/20190228/'}]" />
  </div>  
    <img src="./assets/maneater-full-length.jpg"  class="photo-full-length drop-shadow"/>
</template>

<script>
import ContentWindow from './components/ContentWindow.vue'

export default {
  name: 'App',
  components: {
    ContentWindow
  }, 
}

</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Share+Tech+Mono&display=swap');
body {
  width: 100vw;
  height: 100vh;
}
body {
  background-color: #bde0fe;

}
#app {
  font-family: 'Share Tech Mono', monospace;
  color: #D27774;
  height: 300vh;
  display: flex ;
  flex-direction: column;
  align-items: center;
  text-align: center;
  padding: 4rem 2rem;
}
a:hover {
  color: #42b983;
}
.background-person {
  position: fixed;
  width: 100px;
}

.photo {
  width: 80vw;
  z-index: 1000;
  @media (min-width: 680px) {
    width: 50vw;
  }
}
.photo-full-length {
  width: 80%;
  object-fit: cover;
}
.drop-shadow {
  box-shadow: rgba(0, 0, 0, 0.25) 0px 54px 55px, rgba(0, 0, 0, 0.12) 0px -12px 30px, rgba(0, 0, 0, 0.12) 0px 4px 6px, rgba(0, 0, 0, 0.17) 0px 12px 13px, rgba(0, 0, 0, 0.09) 0px -3px 5px;
}

.banner {
  width: 100%;
  z-index: 1000;

}
.socials {
  list-style: none;
  display: flex;
  z-index: 1000;
  margin-bottom: 4rem;

}
.socials a:hover img{
 background: #42b983;
}
.socials img {
  height: 40px;
  width: 40px;
  border-radius: 50%;
  margin: 5px;
  
}

.content-window-container {
  justify-content: space-around;
  display: flex;
  flex-direction: column;
  z-index: 1000;
  width: 100%;
  @media (min-width: 680px) {
    flex-direction: row;
    margin-bottom: -90px;

  }
}
</style>
