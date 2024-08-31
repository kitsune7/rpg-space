<script lang="ts">
  import SearchIcon from "./search/search-icon.svelte";
</script>

<div>
  <SearchIcon class="search-icon" />
  <input type="search" placeholder="Search..." />
</div>

<style>
  div {
    position: relative;
  }

  div :global(.search-icon) {
    position: absolute;
    top: 50%;
    left: .5rem;
    transform: translateY(-50%);
  }

  input {
    background: transparent;
    border: 1px solid var(--color-gray-400);
    border-radius: .25rem;
    color: var(--color-white);
    padding-left: 2.25rem;
    padding-block: .5rem;
    
    &:hover {
      border-color: var(--color-gray-300);
    }
    
    &:focus {
      outline: 2px solid var(--color-gray-300);
    }
  }
</style>