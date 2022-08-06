<script context="module" lang="ts">
  import type { Load } from "@sveltejs/kit"
  // import('@sveltejs/kit').Load
  export const load:Load =({ error, status }) => {
    return {
      props: {
        title: `${status}: ${error?.message}`
      }
    };
  }
</script>

<script lang="ts">
  export let title:string;
</script>

<svelte:head>
  <title>404 - POKE</title>
</svelte:head>
<h1>{title}</h1>