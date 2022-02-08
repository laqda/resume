<script lang='ts'>
	import Tag from '$lib/Tag.svelte';

	export let tags: string[];
</script>

<div>
	{#each tags as tag}
		<Tag label={tag} />
	{/each}
</div>

<style lang='scss'>
  div {
    display: flex;
		margin-top: 5px;

    & > :global(*:not(:first-child)) {
      margin-left: 5px;
    }
  }
</style>