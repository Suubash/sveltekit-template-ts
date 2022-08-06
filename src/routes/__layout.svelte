<script>
  import "../app.css"
  import Header from "../components/Header.svelte";
</script>

<Header/>
<main class="custom-width py-8">
  <slot/>
</main>