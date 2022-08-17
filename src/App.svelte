<script>
  import noetikaLogo from '/noetika_white_nbg.svg'
  import Main from "./PageMain.svelte";
	import WiHi from "./PageWiHi.svelte";
  import {Route} from 'tinro'; 

</script>

<main>
  <a href="/"><img src={noetikaLogo} class="logo" alt="Noetika Logo" /></a>

  <Route path="/">
    <Main />
  </Route>
  <Route path="/weather">
    <WiHi />
  </Route>
  
  <h6>&copy; 2022 Noetika Technologies d.o.o.
  <br>we stand by our product &mdash we just think we're better</h6>

</main>

<style>
	:global(body) {
		background-color: #0d111d;
		color: #ffffff;
		transition: background-color 0.3s
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
  @media screen and (max-width: 539px) {
    .logo {
      width: 79%;
    }
  }
</style>
