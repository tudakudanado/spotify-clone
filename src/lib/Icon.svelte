<script>
  export let name;
  import { onMount } from "svelte";

  let svgContent = "";

  onMount(async () => {
    try {
      // Динамически импортируем нужный SVG файл
      const svgModule = await import(`../assets/${name}.svg?raw`);
      svgContent = svgModule.default;
    } catch (error) {
      console.error(`Icon "${name}" not found`);
    }
  });

</script>

{#if svgContent}
  {@html svgContent}
{:else}
  <div>Icon not found</div>
{/if}
