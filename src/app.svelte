<svelte:options tag="my-app" />

<h1>Hello {name}!</h1>

<p>Try 'inspect element' — the <code>Box</code> and <code>Counter</code> components have been converted to custom elements with shadow DOM and scoped styles.</p>

<my-box>
	<p>The button has been clicked {count} times</p>
	<my-counter {count} on:click={() => count++}></my-counter>
</my-box>

<my-box>
	Uncontrolled counter:<br>
	<my-counter></my-counter>
</my-box>

<style>
	h1 {
		color: purple;
	}

	code {
		font-family: Menlo, Inconsolata, monospace;
		font-size: 14px;
		background-color: #f0f0f0;
		border-radius: 2px;
		padding: 2px 5px;
	}
</style>

<script>
	import './box.svelte';
	import './counter.svelte';

	let count = 0
	export let name
</script>
