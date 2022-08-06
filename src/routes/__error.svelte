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
<p>Page not found!! Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempora earum fugiat quis, illum distinctio quibusdam beatae? Consectetur temporibus sapiente debitis?</p>