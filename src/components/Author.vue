<template>
	<div class="author">

		<g-image alt="Author image" class="author__image" src="~/assets/images/profile.jpg" width="180" height="180" blur="5" />

		<a href="/" style="text-decoration : none;">
			<h1 v-if="showTitle" class="author__site-title" style="text-decoration : none;">
				{{ $static.metadata.siteName }}
			</h1>
		</a>

		<p class="author__intro">
			{{ $static.metadata.siteDescription }}
		</p>
		
		<p class="author__links">
			<a href="https://www.linkedin.com/in/muhammad-burhanudin-yusuf-395633125/">Linkedin</a>
			<a href="/about-me/">About Me</a>
			<a href="//github.com/hanzkid">GitHub</a>
		</p>

	</div>
</template>

<static-query>
query {
  metadata {
    siteName,
    siteDescription
  }
}
</static-query>

<script>
export default {
	props: ['showTitle']
}
</script>

<style lang="scss">
.author {
	margin: 0 auto;
	max-width: 500px;
	text-align: center;
	padding: calc(var(--space) / 2) 0;

	&__image {
		border-radius: 100%;
		width: 90px;
		height: 90px;
		margin-bottom: 1em;
	}

	&__intro {
		opacity: .8;
	}

	&__site-title {
		font-size: 1.5em;
	}

	&__links {
		margin-top: -.5em;
		a {
			margin: 0 .5em;
		}
	}
}
</style>
