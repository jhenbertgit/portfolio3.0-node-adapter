<script lang="ts">
	export let meta: Meta;
	export let pathname;
</script>

<svelte:head
	><title>{meta.title}</title>
	<!-- Meta Tags -->
	<meta name="title" content={meta.title} />
	<meta name="description" content={meta.description} />
	<meta
		name="keywords"
		content="affordable web developer in the Philippines, SvelteKit developer portfolio in Davao, freelance web developer Davao portfolio, full-stack developer Philippines portfolio, Philippines-based Svelte developer, hire SvelteKit developer in Davao, SvelteKit developer Philippines, remote SvelteKit developer Philippines, affordable SvelteKit development Philippines"
	/>
	<meta name="author" content="Jhenbert" />
	<!-- Open Graph - https://ogp.me/ -->
	<meta property="og:site_name" content="Jhenbert's Portfolio Website" />
	<meta property="og:type" content="website" />
	<meta property="og:url" content="https://jhenbert.com{pathname}" />
	<meta property="og:locale" content="en_PH" />
	<meta property="og:title" content={meta.title} />
	<meta property="og:description" content={meta.description} />
	<meta property="og:image" content={meta.image} />
	<meta property="og:image:secure_url" content={meta.image} />
	<meta property="og:image:type" content="image/jpg" />
	<meta property="og:image:width" content="460" />
	<meta property="og:image:height" content="460" />
	<meta property="og:image:alt" content="Photo" />
	<!-- Open Graph: Twitter -->
	<meta name="twitter:card" content="summary" />
	<meta name="twitter:site" content="@f0rty9er" />
	<meta name="twitter:creator" content="@f0rty9er" />
	<meta name="twitter:title" content={meta.twitter.title} />
	<meta name="twitter:description" content={meta.twitter.description} />
	<meta name="twitter:image" content={meta.twitter.image} />
</svelte:head>
