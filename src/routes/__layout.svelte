<script context='module'>
	import { init, register, waitLocale } from 'svelte-intl-precompile';

	register('fr', () => import('$locales/fr.js'));
	register('en', () => import('$locales/en.js'));

	export async function load() {
		init({
			initialLocale: 'en',
			fallbackLocale: 'fr'
		});
		await waitLocale(); // awaits for initialLocale language pack to finish loading;
		return {};
	}
</script>

<slot />