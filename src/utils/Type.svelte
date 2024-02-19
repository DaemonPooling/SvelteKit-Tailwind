<script>
    /* TODO: Fix this */

    import { onMount, afterUpdate } from 'svelte';
    let element;
    let displayText = '';
    export let _class = ''
    export let text = '';
  
    const animateText = () => {
      let i = 0;
      setInterval(() => {
        if (i <= text.length) {
          displayText = text.slice(0, i);
          i++;
        } else {
          i = 0;
        }
      }, 500);
    };
  
    onMount(animateText);
    afterUpdate(animateText);
</script>
  
<div class={_class} bind:this={element}>
  {displayText}
</div>
