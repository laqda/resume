<script lang='ts'>
	import TagList from '$lib/TagList.svelte';

	export let tags: string[];
</script>

<div class='sub-sub-section'>
	<div class='content'>
		<slot />
	</div>
		<TagList tags={tags} />
</div>

<style lang='scss'>
  .sub-sub-section {
    margin-top: 5px;
  }
</style>