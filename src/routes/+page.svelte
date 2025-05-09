<script>
  import "../app.css";
  import Navbar from "../lib/Navbar.svelte";
  import TextIncident from "../incident.txt?raw";
  import Box from "../lib/Box.svelte";
  import IconSearx from "../lib/assets/searxng.svg";
  import IconPrivatebin from "../lib/assets/privatebin.png";
  import IconHyperpipe from "../lib/assets/hyperpipe.png";
  import IconVaultwarden from "../lib/assets/vaultwarden.png";
  import IconLibrarian from "../lib/assets/librarian.png";
  import IconLibrespeed from "../lib/assets/librespeed.png";
  import IconJitsi from "../lib/assets/jitsi.png";
  function redirectToLink(link) {
    window.location.href = link;
  }
</script>

<Navbar />

<h1>Services</h1>

<div class="container">
  <div class="box" onclick="window.open('https://search.ramondia.net/', '_blank')">
    <h2>SearXNG</h2>
    <img
      src={IconSearx}
      alt="SearXNG"
      class="image"
      border="0"
    />
    <p>A Private Meta-Search Engine.</p>
  </div>

  <div
    class="box"
    onclick="window.open('https://privatebin.ramondia.net/', '_blank')"
  >
    <h2>PrivateBin</h2>
    <img
      src={IconPrivatebin}
      alt="PrivateBin"
      class="image"
      border="0"
    />
    <p>Pastebin's Privacy-Friendly Alternative.</p>
  </div>

  <div
    class="box"
    onclick="window.open('https://vault.ramondia.net/', '_blank')"
  >
    <h2>Vaultwarden</h2>
    <img
      src={IconVaultwarden}
      alt="Vaultwarden"
      class="image"
      border="0"
    />
    <p>A Password Manager.</p>
  </div>

  <div
    class="box"
    onclick="window.open('https://lbry.ramondia.net/', '_blank')"
  >
    <h2>Librarian</h2>
    <img
      src={IconLibrarian}
      alt="Librarian"
      class="image"
      border="0"
    />
    <p>A Frontend For Odysee.</p>
  </div>

  <div class="box" onclick="window.open('https://speed.ramondia.net/', '_blank')">
    <h2>LibreSpeed</h2>
    <img
      src={IconLibrespeed}
      alt="LibreSpeed"
      class="image"
      border="0"
    />
    <p>Privacy-Focused Internet Speed Test Service.</p>
  </div>

  <div class="box" onclick="window.open('https://jitsi.ramondia.net/', '_blank')">
    <h2>Jitsi</h2>
    <img
      src={IconJitsi}
      alt="Jitsi"
      class="image"
      border="0"
    />
    <p>Video Conferencing Software.</p>
  </div>
</div>

<h1>Incidents</h1>

<div class="incidentbox">
  <p>{TextIncident}</p>
  </div>

<style>
  .container {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    margin: 0.5em;
  }

  .box {
    width: 300px;
    border: 1.5px solid #3d3c3c;
    border-radius: 1px;
    box-shadow: 1px 1px 4px rgba(0, 255, 255, 0.24);
    padding: 1em;
    margin: 0.5em;
    cursor: pointer;
    border-radius: 5%;
  }
  .incidentbox {
    display:flex;
    width: 300px;
    border: 1.5px solid #3d3c3c;
    box-shadow: 1px 1px 4px rgba(0, 255, 255, 0.24);
    padding: 1em;
    margin: auto;
    cursor: pointer;
  }

  .box:hover {
    opacity: 0.8;
    background-color: rgb(19, 18, 18);
  }

  .box:not(:last-child) {
    margin-right: 1em;
  }

  .box h2 {
    margin-top: 3px;
    color: rgba(0, 255, 255, 0.726);
  }
  .box p {
    margin-top: auto;
    margin-bottom: auto;
    color: rgb(207, 203, 203);
  }
  .container img {
    width: 25%;
    height: auto;
    object-fit: cover;
  }

  .image {
    float: left;
    margin-right: 30px;
  }
</style>
