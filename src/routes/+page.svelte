<script lang="ts">
  import { ChevronDown } from "lucide-svelte";

  let showIcon = $state(false);

  $effect(() => {
    setTimeout(() => {
      showIcon = true;
    }, 1000);
  });
</script>

<h1>Welcome to SvelteKit</h1>
<p>
  Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation
</p>

<p>Server Rendered Icon</p>
<ChevronDown size="64" />
{#if showIcon}
  <p>Browser Rendered Icon</p>
  <ChevronDown size="64" />
{/if}
