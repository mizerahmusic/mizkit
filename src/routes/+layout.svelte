<script lang="ts">
	import 'greset/greset.css'
	import '../styles/app.scss'

	import Header from '$lib/components/Header/Header.svelte'
	import PageTitle from '$lib/components/PageTitle.svelte'
	import { Fractils, theme } from 'fractils'
	import { browser } from '$app/environment'

	$: if (browser) {
		document.cookie = `theme=${$theme}`
	}
</script>

<PageTitle />

<Fractils />

<Header />

<div class="br-md" />

<slot />
