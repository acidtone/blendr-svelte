<script>
  export let name;
  export let max = 100;
  export let min = 0;
  export let defaultValue;
  export let unit = '';

  const handleInput = (evt) => {
    document.documentElement.style.setProperty(`--${name}`, `${evt.target.value}${unit}`);
  }
</script>

<label for="{name}" on:input={handleInput}>
  <span class="label">{name}</span>
  <input id="{name}" name="{name}" type="range" {min} {max} value={defaultValue}>
</label>