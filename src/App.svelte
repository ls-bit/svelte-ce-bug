<script>
  import { onMount } from 'svelte';
  import Test from './Test.svelte';

  let container;

  onMount(() => {
    if (!window.customElements.get('ce-test')) {
        window.customElements.define('ce-test', Test.element);
    }

    const customElement = document.createElement('ce-test');

    customElement.name = 'accessor-name';
    customElement.other = 'accessor-other';

    container.appendChild(customElement);
  })

</script>
 
<ce-test name="attribute-name" other="attribute-other"></ce-test>

<div bind:this={container} />