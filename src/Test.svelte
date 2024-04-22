<svelte:options
    customElement={{
        tag: null,
    }}
/>
<script>
	export let name;
</script>

<p>$$props: {JSON.stringify($$props)}</p>
<p>$$restProps: {JSON.stringify($$restProps)}</p>