<script>
  import SocialIcons from '@rodneylab/svelte-social-icons';
  import noetikaLogo from '/noetika_white_nbg.svg'
  import urosHeadshot from './assets/uros_headshot.jpg'
  import mikeHeadshot from './assets/mike_headshot.jpg'

  $: innerWidth = 0

  let socialIconWidth = 28;
  let socialIconHeight = 28;
  let can = "can";

  const cantDo = () => {can = "can't"};
  const canSwitch = () => {can = can === "can't" ? "can" : "can't"};

  const social = [
    { network: "linkedin", uk: "https://www.linkedin.com/in/ukalabic/", mc: "https://www.linkedin.com/in/chiumichael/"},
    { network: "telegram", uk: "https://t.me/urosvk", mc: "https://t.me/m1ch5ael"}, 
    { network: "mailto", uk: "mailto:uros@noetika.tech", mc: "mailto:mike@noetika.tech"}
  ];

</script>

<svelte:window bind:innerWidth />

<main>
  <img src={noetikaLogo} class="logo" alt="Noetika Logo" />

  <h1>Welcome to noëtic engineering</h1>
  <p>
    Noetika Technologies is a boutique blockchain shop
    specializing in connecting distributed systems with the real world.
    {#if innerWidth > 906} <br> {/if}
    Our achievements include web3 development for weather, space, and industrial applications.
  </p>

  <h2>Our co-founders:</h2>

  <div class="people">
    <div>
      <img src={urosHeadshot} class="headshot" alt="Uros Kalabic" />
      <br><strong>Uroš V. Kalabić, PhD, CEO</strong>
      <br>software development, operations, research
      <div class="socials">
      {#each social as { network, uk }}
      <div class="icon">
        <a href={uk} target="_blank"><SocialIcons {network} width={socialIconWidth} height={socialIconHeight} /></a>
      </div>
      {/each}
      </div>
    </div>
    <div>
      <img src={mikeHeadshot} class="headshot" alt="Michael Chiu" />
      <br><strong>Michael Chiu, CTO</strong>
      <br>software & business development
      <div class="socials">
      {#each social as { network, mc }}
      <div class="icon">
        <a href={mc} target="_blank"><SocialIcons {network} width={socialIconWidth} height={socialIconHeight} /></a>
      </div>
      {/each} 
      </div>
    </div>
  </div>

  <h1 on:mouseover={cantDo} on:focus={cantDo} on:mousedown={canSwitch}>What {can} we do for you?
    <br><a href= "mailto: mail@noetika.tech">Contact us</a>
  </h1>

  <h6>&copy; 2022 Noetika Technologies d.o.o.
  <br>we stand by our product &mdash we just think we're better</h6>

</main>

<style>
	:global(body) {
		background-color: #0d111d;
		color: #ffffff;
		transition: background-color 0.3s
	}
	:global(h2) {
    font-size: 2.5em;
	}
  .logo {
    width: 426px;
    padding: 1.5em;
    /*will-change: filter;*/
    filter: drop-shadow(0 0 2em #646cffaa) drop-shadow(0 0 2em #646cffaa) drop-shadow(0 0 2em #646cffaa) drop-shadow(0 0 2em #646cffaa);
  }
  .logo:hover {
    filter: drop-shadow(0 0 2em #ff3e00aa) drop-shadow(0 0 2em #ff3e00aa) drop-shadow(0 0 2em #ff3e00aa) drop-shadow(0 0 2em #ff3e00aa);
  }
  .headshot {
    width: 240px;
    padding: 16px;
    border: 1px;    
    border-radius:100%;
  }
  .people {
    display: flex;
    justify-content: space-evenly; 
  }
  @media screen and (max-width: 576px) {
    .people {
      flex-direction: column;
    }
  }
  @media screen and (max-width: 539px) {
    .logo {
      width: 79%;
    }
  }

  .socials {
    display: flex;
    justify-content: center;
  }
  .icon {
    margin-left: 5px;
    margin-right: 5px;
    margin-top: 5px;
  }
  .icon:hover {
    opacity:0.5;
  }
</style>
