<script lang='ts'>
	import Fa from 'svelte-fa/src/fa.svelte';
	import type { IconDefinition } from '@fortawesome/fontawesome-common-types';

	export let title: string;
	export let icon: IconDefinition;
</script>

<div class='section'>
	<div class='title'>
		<h1>
			<Fa icon={icon} />
			<span>{title}</span>
		</h1>
	</div>
	<div class='content'>
		<slot />
	</div>
</div>

<style lang='scss'>
  .section {
    margin: 10px 0 0;

    & > .title {
      display: flex;
      align-items: center;

      color: var(--primary);

      & > h1 > :global(svg) {
        margin-right: 6px;
      }
    }

    & > .content {
      margin: 15px 5px 0;
			font-size: 14px;
    }
  }
</style>