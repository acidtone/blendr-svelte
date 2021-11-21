<script>
  let blendModes = [
    // TODO: add descriptions, equations, etc to each blend mode item; move code to a json thing
    {
      name: 'normal',
    },
    {
      name: 'multiply',
    },
    {
      name: 'screen',
    },
    {
      name: 'overlay',
    },
    {
      name: 'darken',
    },
    {
      name: 'lighten',
    },
    {
      name: 'color-dodge',
    },
    {
      name: 'color-burn',
    },
    {
      name: 'hard-light',
    },
    {
      name: 'soft-light',
    },
    {
      name: 'difference',
    },
    {
      name: 'exclusion',
    },
    {
      name: 'hue',
    },
    {
      name: 'saturation',
    },
    {
      name: 'color',
    },
    {
      name: 'luminosity',
    }
  ];

</script>
<section>
  {#each blendModes as mode}
    <article style="background-blend-mode: {mode.name}">
      {mode.name}
    </article>
  {/each}
</section>
<style>
  section {
    aspect-ratio: 1;    
    max-height: 90vmin;
    padding: 0.5em;
    border-radius: 0.5em;
    margin: auto;

    display: grid;
    grid-template-columns: repeat(4, minmax(20ch, 1fr));
    grid-template-rows: repeat(4, 1fr);
    grid-gap: 0.5em;
  }

  article {
    position: relative;
    background-color: var(--primary-clr);
    background-image: url('https://picsum.photos/3000/3000');
    background-size: cover;
    background-position: center center;
  }
</style>