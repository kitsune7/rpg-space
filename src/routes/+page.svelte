<script lang="ts">
  import SearchInput from "$lib/search-input.svelte";
  import { onMount } from "svelte";

  let data: Record<string, any> | null = null;

  onMount(async () => {
    const res = await fetch('/api');
    data = await res.json();
  })
</script>

<header>
  <h1>RPG Space</h1>
  <SearchInput />
</header>
<main>
</main>

<style>
  header {
    align-items: center;
    background-color: var(--color-gray-950);
    color: var(--color-white);
    display: flex;
    justify-content: space-between;
    padding: 1rem;
  }

  h1 {
    font-family: var(--font-family-mono);
    margin: 0;
  }
</style>