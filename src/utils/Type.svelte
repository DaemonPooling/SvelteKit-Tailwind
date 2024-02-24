<script>
  import { onMount } from 'svelte';

  export let text = 'Hello guys!';
  var displayText = ''
  export let duration = 50
  export let wait = 0

  function sleep(ms) {
    return new Promise(resolve => setTimeout(resolve, ms));
  }

  onMount(async () => {
    for (let part of text.split(' ')) {
      displayText = '';
      await type(part);
      await sleep(wait);
    }
  })

  async function type(part) {
    for (let i = 0; i < part.length; i++) {
      displayText += part[i];
      await sleep(duration);
    }
  }
</script>

<span>
  {displayText}
</span>
