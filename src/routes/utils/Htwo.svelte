<script>
	import { Link } from 'svelte-heros';
	export let label;
	let modifiedLabel = label.replace(/\s/g, '_');
	let hidden = true;
	const handleMouseover = () => {
		hidden = false;
	};
	const handleMouseout = () => {
		hidden = true;
	};
</script>

<h2
	class="htwo text-2xl w-full font-semibold dark:text-white mb-4 mt-8"
	on:mouseover={handleMouseover}
	on:focus
	on:mouseout={handleMouseout}
	on:blur
	id={modifiedLabel}
>
	<a href="#{modifiedLabel}" class="relative w-4 h-4" aria-label={label}>
		<span class:hidden class="absolute right-0"><Link size="20" /></span>
	</a>{label}
</h2>
