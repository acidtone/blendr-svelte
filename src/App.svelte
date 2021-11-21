<script>
  import PrimaryClr from './components/Hsl.svelte';
  import Blendmodes from './components/Blendmodes.svelte';

  let instructions = "Primary Colour";
</script>

<aside>
  <PrimaryClr {instructions}/>
</aside>
<main>
  <Blendmodes/>
</main>