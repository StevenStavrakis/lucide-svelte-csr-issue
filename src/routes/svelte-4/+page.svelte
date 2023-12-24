<script>
  import { ChevronDown } from "lucide-svelte";
  import { onMount } from "svelte";

  let showIcon = false;
  onMount(() => {
    setTimeout(() => {
      showIcon = true;
    }, 1000);
  });
</script>

<p>Server rendered icon</p>
<p>Will work if you reload page to force SSR</p>
<ChevronDown size="64" />
{#if showIcon}
  <p>Browser Rendered Icon</p>
  <ChevronDown size="64" />
{/if}
