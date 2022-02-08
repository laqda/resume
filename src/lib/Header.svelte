<div class="header">
	<div class="img-container">
		<slot name="img" />
	</div>
	<div class="content">
		<div class="infos">
			<h2 class="name">
				<slot name="name" />
			</h2>
			<div class="address">
				<slot name="address" />
			</div>
			<div class="links">
				<slot name="links" />
			</div>
			<div class="side">
				<slot name="side" />
			</div>
		</div>
	</div>
</div>

<style lang="scss">
	.header {
		display: flex;
		height: 160px;
		padding: 15px;
		background-color: var(--primary);
		color: white;
		line-height: 1.4rem;

		& > .img-container {
			width: fit-content;

			& > :global(img) {
				max-height: 100%;
			}

			&:empty {
				margin-right: 5px;
			}
		}
	}

	.content {
		display: flex;
		flex: 1 1 0;
		padding: 0 20px;
		align-items: center;

		& > .infos {
			flex: 1 1 0;

			display: grid;
			grid-template-rows: auto auto auto;
			grid-template-columns: auto auto;
			grid-gap: 10px;

			& > .name {
				grid-row: 1;
				grid-column: 1;
			}

			& > .address {
				grid-row: 2;
				grid-column: 1;
			}

			& > .links {
				grid-row: 3;
				grid-column: 1;
			}

			& > .side {
				grid-row: 1 / 4;
				grid-column: 2;

				text-align: end;
			}
		}
	}
</style>
