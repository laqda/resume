<div>
	<slot />
</div>

<style lang='scss'>
  div {
    min-width: 21cm;
    max-width: 21cm;
    max-height: 29.7cm;
    min-height: 29.7cm;
    overflow: hidden;

    display: flex;
		flex-direction: column;

		background-color: white;
  }
</style>