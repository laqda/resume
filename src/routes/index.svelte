<script>
	import Header from '$lib/Header.svelte';
	import Page from '$lib/Page.svelte';
	import Fa from 'svelte-fa/src/fa.svelte';
	import {
		faChessBishop,
		faEnvelope,
		faGlobe,
		faPhone,
		faSuitcase,
		faUserGraduate
	} from '@fortawesome/free-solid-svg-icons';
	import { faGithub } from '@fortawesome/free-brands-svg-icons';
	import HeaderLinks from '$lib/HeaderLinks.svelte';
	import Section from '$lib/Section.svelte';
	import SubSection from '$lib/SubSection.svelte';
	import SubSubSection from '$lib/SubSubSection.svelte';

	import { t, locale } from 'svelte-intl-precompile';
</script>

<Page>
	<Header>
		<svelte:fragment slot="img">
			{#if $locale === 'fr'}
				<img src="/profil.jpg" alt="profil" />
			{/if}
		</svelte:fragment>

		<svelte:fragment slot="name">Quentin MICHEL</svelte:fragment>
		<svelte:fragment slot="address">
			{$t('header.address.line1')}<br />
			{$t('header.address.line2')}
		</svelte:fragment>
		<svelte:fragment slot="links">
			<HeaderLinks>
				<Fa icon={faPhone} />
				<span>+33 6 89 29 48 18</span>

				<Fa icon={faEnvelope} />
				<span>quentinmichel69110@gmail.com</span>

				<Fa icon={faGithub} />
				<span>https://github.com/laqda</span>
			</HeaderLinks>
		</svelte:fragment>

		<svelte:fragment slot="side">
		</svelte:fragment>
	</Header>

	<div class="content">
		<Section icon={faSuitcase} title={$t('xp.title')}>
			<SubSection
				title={$t('xp.armed_forces.title')}
				organization={$t('xp.armed_forces.organization')}
				location={$t('xp.armed_forces.location')}
				duration={$t('xp.armed_forces.duration')}
			>
				<SubSubSection
					tags={['React', 'Angular', 'Flux', 'RxJs', 'Quarkus', 'MySQL', 'Kubernetes']}
				>
					{$t('xp.armed_forces.section1.line1')}<br />
					{$t('xp.armed_forces.section1.line2')}<br />
					{$t('xp.armed_forces.section1.line3')}<br />
					{$t('xp.armed_forces.section1.line4')}
				</SubSubSection>

				<SubSubSection tags={['Rust', 'Tokio', 'Reqwest', 'Oracle', 'Kubernetes']}>
					{$t('xp.armed_forces.section2.line1')}
				</SubSubSection>

				<SubSubSection tags={['Rust', 'GraphQL', 'Actix', 'Gremlin']}>
					{$t('xp.armed_forces.section3.line1')}
				</SubSubSection>
			</SubSection>

			<SubSection
				title={$t('xp.akoute.title')}
				organization={$t('xp.akoute.organization')}
				location={$t('xp.akoute.location')}
				duration={$t('xp.akoute.duration')}
			>
				<SubSubSection tags={['React', 'Redux', 'Electron', 'MaterialUI', 'D3.js']}>
					{$t('xp.akoute.section1.line1')}
				</SubSubSection>
			</SubSection>

			<SubSection
				title={$t('xp.hda.title')}
				organization={$t('xp.hda.organization')}
				location={$t('xp.hda.location')}
				duration={$t('xp.hda.duration')}
			>
				<SubSubSection tags={['Go', 'GraphQL', 'Wordpress']}>
					{$t('xp.hda.section1.line1')}
				</SubSubSection>
			</SubSection>

			<SubSection
				title={$t('xp.junior.title')}
				organization={$t('xp.junior.organization')}
				location={$t('xp.junior.location')}
				duration={$t('xp.junior.duration')}
			>
				<SubSubSection tags={['React', 'Redux', 'Wordpress']}>
					{$t('xp.junior.section1.line1')}
				</SubSubSection>
			</SubSection>
		</Section>

		<Section icon={faUserGraduate} title={$t('study.title')}>
			<SubSection
				title={$t('study.cs.title')}
				organization={$t('study.cs.organization')}
				location={$t('study.cs.location')}
				duration={$t('study.cs.duration')}
			>
				<SubSubSection
					tags={[
						$t('study.cs.tags.os'),
						'Linux',
						'ASM',
						$t('study.cs.tags.compilation'),
						$t('study.cs.tags.cryptography'),
						'Ghidra'
					]}
				>
					{$t('study.cs.section1.line1')}
				</SubSubSection>
			</SubSection>

			<SubSection
				title={$t('study.isep.title')}
				organization={$t('study.isep.organization')}
				location={$t('study.isep.location')}
				duration={$t('study.isep.duration')}
			>
				<SubSubSection tags={['Java', 'Web', $t('study.isep.tags.algorithmics')]}>
					{$t('study.isep.section1.line1')}
				</SubSubSection>
			</SubSection>
		</Section>

		<div class="side-by-side">
			<Section icon={faGlobe} title={$t('languages.title')}>
				{#if $locale !== 'fr'}
					{$t('languages.french.title')} - {$t('languages.french.label')}<br />
				{/if}
				{$t('languages.english.title')} - {$t('languages.english.label')} <i>(TOEIC : 930)</i><br />
				{#if $locale === 'fr'}
					{$t('languages.deutsch.title')} - {$t('languages.deutsch.label')}<br />
				{/if}
			</Section>

			<Section icon={faChessBishop} title={$t('hobbies.title')}>
				{$t('hobbies.sports.title')} - <i>{$t('hobbies.sports.list')}</i><br />
				{$t('hobbies.trips.title')} - <i>{$t('hobbies.trips.list')}</i><br />
			</Section>
		</div>
	</div>
</Page>

<style lang="scss">
	.content {
		flex: 1 1 0;
		justify-content: center;

		padding: 0 40px;

		display: flex;
		flex-direction: column;

		line-height: 1.1rem;
	}

	.side-by-side {
		display: flex;

		& > :global(*) {
			flex: 1 1 0;
		}
	}
</style>
