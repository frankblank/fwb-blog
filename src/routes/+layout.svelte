<script lang="ts">
	import { page } from '$app/stores'
	import { handleSession } from '@lucia-auth/sveltekit/client'
	import Heading from './heading.svelte'
	import Footer from './footer.svelte'

	import '@skeletonlabs/skeleton/themes/theme-crimson.css'
	import '@skeletonlabs/skeleton/styles/all.css'
	import '../app.postcss'

	handleSession(page)
</script>

<svelte:head>
	<title>Frank Blank</title>
	<link rel="icon" href="%sveltekit.assets%/favicon.png" />
</svelte:head>

<Heading />
<slot />
<Footer />
