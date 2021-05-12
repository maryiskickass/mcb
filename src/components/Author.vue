<template>
	<div class="author">

		<g-image alt="Author image" class="author__image" src="~/assets/images/mary.gif" width="180" height="180" blur="5" />

		<h1 v-if="showTitle" class="author__site-title">
			{{ $static.metadata.siteName }}
		</h1>

		<p class="author__intro">
      I am a digital media professional currently based in Barcelona, Spain.
    </p>
		<p class="author__intro">
      I leverage my 12+ years of online advertising experience to help companies of all sizes maximize their revenue.
    </p>
		<p class="author__intro">
      I'm passionate about integrity, equality and diversity - and how a focus on purposeful inclusion in the workplace will bring success for both employers and employees.
    </p>

		<p class="author__links">
			<a href="//twitter.com/maryiskickass">Follow on Twitter</a>
      <a href="//linkedin.com/in/marycatherinebrannen">LinkedIn</a>
			<a href="//github.com/maryiskickass">GitHub</a>
		</p>

	</div>
</template>

<static-query>
query {
  metadata {
    siteName
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
