<script>
  import SidebarRight from "./lib/SidebarRight.svelte";
  import SidebarLeft from "./lib/SidebarLeft.svelte";
  import Footer from "./lib/Footer.svelte";
  import MainContent from "./lib/MainContent.svelte";
  import "./app.css";
</script>

<main class="layout flex">
  <MainContent />
  <SidebarLeft />
  <SidebarRight />
  <Footer />
</main>

<style lang="postcss">

</style>
