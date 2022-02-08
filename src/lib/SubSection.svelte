<script lang='ts'>
	export let title: string;
	export let organization: string;
	export let location: string;
	export let duration: string;
</script>

<div class='sub-section'>
	<h3>{title} - {organization} - {location}</h3>
	<div class='duration'>{duration}</div>
	<div class='content'>
		<slot />
	</div>
</div>

<style lang='scss'>
  .sub-section {
		margin: 18px 5px;

    display: grid;
    grid-template-rows: auto auto;
    grid-template-columns: auto 120px;
    grid-template-areas:
			'title duration'
			'content content';

    & > h3 {
      grid-area: title;
    }

    & > .duration {
      grid-area: duration;
			justify-self: end;

			color: #555555;
			font-style: italic;
    }

    & > .content {
      grid-area: content;
			color: #555;
    }
  }
</style>