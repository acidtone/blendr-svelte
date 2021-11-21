<script>
  import Slider from './Slider.svelte';

  export let instructions = 'Edit this colour!';

  let hue = {
    name: 'hue',
    max: 360,
    defaultValue: 180,
    unit: 'deg'
  };

  let sat = {
    name: 'sat',
    max: 100,
    defaultValue: 100,
    unit: '%'
  };

  let lum = {
    name: 'lum',
    max: 100,
    defaultValue: 50,
    unit: '%'
  }

</script>

<fieldset>
  <legend>{instructions}</legend>
  <div class="output"></div>
  <Slider {...hue}/>
  <Slider {...sat}/>
  <Slider {...lum}/>
</fieldset>

<style>
  .output {
    width: 100%;
    aspect-ratio: 1;
    background-color: var(--primary-clr);
  }
</style>