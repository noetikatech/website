<script>
    import WhitePaper from './assets/wihi_whitepaper_160822.pdf'
    import Presentation from './assets/wihi_presentation_160822.pdf'
    import MicroSchematic from './assets/how_wihi_works.png'
    import WiHiLogo from './assets/wihi_logo.jpeg'
</script>

<h1>Welcome to WiHi
</h1>
<h2>
<i>Winner of the 2022 Solana Summer Camp Hackathon
<a href="https://solana.com/news/solana-summer-camp-winners">Climate Award</a></i>
</h2>

<div class="text-block">

<img src={WiHiLogo} class="logo" alt="WiHi Logo" />

<p>
  WiHi is a decentralized solution to the problems of weather forecasting and climate monitoring.
  It comes with an algorithm that measures contributions to forecast improvement and pays out participants in proportion to how much improvement their sensors provide.
</p>

<h2>How does it work?</h2>

<p>
WiHi rewards data providers in proportion to how much their data improve the forecast.
The rewards are computed according to a "post-processing" algorithm that assimilates forecasts
(based on publicly available data) with WiHi sensor data.
</p>

<img src={MicroSchematic} class="schematic">
</div>


<h2>Why do I want to use WiHi?</h2>

<div class="text-block" style="text-align:left;">
  <p>
  If you are a manufacturer of weather sensors...
  <br><span style="float:right;">...WiHi increases the value of your product.</span>
  <br>
</p>

<p>
  If you are looking to run a    sensor...
  <br><span style="float:right;">...WiHi pays you for your data.</span>
  <br>
</p>

<p>
  If you are the general public...
  <br><span style="float:right;">...WiHi improves our understanding of weather (and gives better forecasts).</span>
  <br>
</p>

<p>
  If you like Solana...
  <br><span style="float:right;">...WiHi is part of the Solana ecosystem.</span>
</p>
</div>

<h2>Click a link below to learn more:</h2>

<span style="font-size:2em">
<p>
<a href="https://vimeo.com/740243385" target="_blank">presentation</a>
</p>

<p>
<a href={Presentation} target="_blank">slides</a>
</p>

<p>
<a href={WhitePaper} target="_blank">whitepaper</a>
</p>
</span>

<style>
  .schematic {
    width: 550px;
  }
  .logo {
    width: 300px;
    padding: 1.5em;
    border-radius: 45px;
    /*will-change: filter;*/
  }
  @media screen and (max-width: 650px) {
    .schematic {
      width: 100%;
    }
    .logo {
      width: 46%;
    }
  }
</style>
