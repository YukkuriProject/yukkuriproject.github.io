<script>
  import { base } from "$app/paths";
  import { page } from "$app/stores";
</script>

<header>ISOJIN</header>

<nav>
  <a
    href="{base}/"
    aria-current={$page.url.pathname === base + "/"}
    class="nav-element">トップ</a
  >
  <a
    href="{base}/kendomod"
    aria-current={$page.url.pathname === base + "/kendomod"}
    class="nav-element">剣道Mod</a
  >
  <a
    href="{base}/maidillager"
    aria-current={$page.url.pathname === base + "/maidillager"}
    class="nav-element">MaidIllager</a
  >
  <a
    href="{base}/whistlemod"
    aria-current={$page.url.pathname === base + "/whistlemod"}
    class="nav-element">WhistleMod</a
  >
</nav>

<slot />

<footer>
  <!-- AddToAny BEGIN -->
  <div class="a2a_kit a2a_kit_size_32 a2a_default_style share_buttons">
    <a class="a2a_dd" href="https://www.addtoany.com/share"></a>
    <a class="a2a_button_mastodon"></a>
    <a class="a2a_button_threads"></a>
    <a class="a2a_button_line"></a>
    <a class="a2a_button_facebook"></a>
    <a class="a2a_button_x"></a>
    <a class="a2a_button_copy_link"></a>
  </div>
  <script async src="https://static.addtoany.com/menu/page.js"></script>
  <!-- AddToAny END -->
</footer>

<style>
  @import url(http://fonts.googleapis.com/earlyaccess/notosansjp.css);

  header {
    font-size: 2em;
    padding-top: 10px;
    background-color: steelblue;
    color: black;
    -webkit-text-stroke: white 1px;
    text-align: center;
    font-weight: bold;
    font-family: "Noto Sans JP", sans-serif;
  }

  nav {
    padding: 10px;
    background-color: #e3e3e3;
    text-align: center;
    font-family: "Noto Sans JP", sans-serif;
  }

  footer {
    position: sticky;
    top: 100vh;
    width: 100%;
    height: 5em;
    background-color: steelblue;
  }

  .share_buttons {
    position: absolute;
    margin-top: 0.5em;
    left: 50%;
    transform: translateX(-50%);
  }

  a.nav-element {
    margin: auto 1em auto;
    color: black;
    text-decoration: none;
  }

  a.nav-element[aria-current="true"] {
    border-bottom: 2px solid;
  }

  /*:root {
    background-image: url(/images/2_20240121190530_1.png);
    background-size: 25%;
  }/*
</style>
