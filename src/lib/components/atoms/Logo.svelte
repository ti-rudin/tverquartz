<script>
	export let animated = true;
</script>

<div class="logo" class:animated>
	<svg
		id="logo-text"
		width="50"
		height="50"
		viewBox="0 0 94 94"
		fill="none"
		xmlns="http://www.w3.org/2000/svg"
	>
		<path
			fill-rule="evenodd"
			clip-rule="evenodd"
			d="M93.0386 0V88.5422L59.1295 39.3636H58.5386V93.0909H36.0386V0H55.4022L92.0386 53.6364L92.8113 54.7903V0H93.0386Z"
			fill="black"
		/>
		<path d="M92.7977 0H93.0523V88.543L92.8917 88.3203L92.7977 88.1641V0Z" fill="black" />
		<rect x="0" y="0" width="100%" height="100%" stroke="black" />
	</svg>
</div>

<style lang="scss">
	@import '$lib/scss/breakpoints.scss';

	.logo {
		width: auto;
		

		display: flex;
		gap: 16px;
		align-items: center;

		@include for-phone-only {
			gap: 8px;
		}

		

		&:hover {
			
				filter: drop-shadow(0px 0px 3px var(--color--primary));
			
		}
	}

	@media screen and (prefers-reduced-motion: no-preference) {
		.animated {
			#icon {
				> path {
					--text-color: var(--color--text-shade);
					stroke-width: 2;
					animation: svg-text-stroke 3s;
				}

				#darker {
					> path {
						--text-color: var(--color--text);
						stroke-width: 2;
						animation: svg-text-stroke 3s;
					}
				}
			}

			#text {
				animation: svg-text-stroke 3s;
				stroke-width: 2;
				--text-color: var(--color--text);
			}
		}
	}
</style>
