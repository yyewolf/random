<script>
  import ninja from './assets/ninja.png';
  import twitchLogo from './assets/twitch.svg';
  import youtubeLogo from './assets/youtube.svg';
  import kickLogo from './assets/kick.svg';
  import { onMount } from 'svelte';

  // detect hover on image
  onMount(() => {
    const img = document.querySelector('img');
    img.addEventListener('mouseenter', () => {
      setTimeout(() => {
        displayStreams();
      }, 2000);
    });
  });

  function displayStreams() {
    const streams = document.querySelector('.links');
    // change opacity
    streams.style.opacity = 1;
  }
</script>

<main>
  <img class="ninja" src={ninja} alt="buy some internet connection"/>

  <div class="links">
    <a class="link" href="https://www.twitch.tv/ninja" target="_blank">
      <img class="icon" src={twitchLogo} alt="twitch logo"/>
      Twitch
    </a>
    <a class="link" href="https://www.youtube.com/@Ninja/streams" target="_blank">
      <img class="icon" src={youtubeLogo} alt="youtube logo"/>
      Youtube
    </a>
    <a class="link" href="https://kick.com/ninja" target="_blank">
      <img class="icon" style="height:30px; margin-top:10px; margin-bottom:20px;" src={kickLogo} alt="kick logo"/>
      Kick
    </a>
  </div>
</main>