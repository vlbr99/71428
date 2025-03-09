<script>
  let { children } = $props();
  import "@fontsource-variable/geist";
</script>

{@render children()}

<style>
  :global(*) {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "Geist Variable", sans-serif;
  }
</style>
