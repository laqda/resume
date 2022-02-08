<div>
	<slot />
</div>

<style lang='scss'>
  div {
    display: grid;
    grid-template-columns: 25px auto;
		align-items: center;

		& > :global(svg) {
			justify-self: center;
			margin-right: 10px;
		}
  }
</style>