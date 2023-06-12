<script>
  import "../app.postcss";
  import Header from "./Header.svelte";
  import Sidemenu from "./Sidemenu.svelte";
  import "./styles.css";
</script>

<style>
  .sidebar {
    grid-area: sidebar;
  }

  .content {
    grid-area: content;
  }

  .header {
    grid-area: header;
  }

  .footer {
    grid-area: footer;
  }


  .wrapper {
    display: grid;
    grid-template-areas:
    "header header header"
    "sidebar content content"
    "footer footer footer";
    background: #ddd;
    height: 100vh;
  }

</style>

<div class="app">
  <div class="wrapper">
    <div class="box header"><Header /></div>
    <div class="box sidebar"><Sidemenu/></div>
    <div class="box content"><main><slot /></main></div>
    <div class="box footer"><footer></footer></div>
  </div>

</div>
