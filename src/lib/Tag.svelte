<script lang='ts'>
	export let label: string;
</script>

<div>
	{label}
</div>

<style lang='scss'>
  div {
		color: var(--primary);
		border: 1px solid var(--primary);
		border-radius: 5px;
		padding: 2px 5px;
		opacity: 0.6;
		font-size: 12px;
	}
</style>