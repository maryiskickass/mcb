<template>
  <div class="flex flex-col min-h-screen">
    <header class="text-center px-5 py-24">
      <img class="inline-block w-48 h-48" src="/images/mary.jpg"/>
      <h1 class="mt-8 text-4xl font-semibold">Hello! I am Mary.</h1>
      <p class="mt-4 mb-8 text-xl">I'm a sassy assy currently based in Barcelona.</p>
      <p class="mt-4 mb-8 text-xl">I leverage my 12+ years of digital advertising experience to help digital publishers of all sizes maximise their revenue.</p>
      <ul>
        <li
          v-for="(link, index) in socialLinks"
          :key="index"
          class="inline-block mx-4"
        >
          <a class="icon-small" :href="link.url" target="_new">
            <img :src="`images/icons/${link.icon}.svg`" class="w-8"/>
          </a>
        </li>
      </ul>
    </header>
    <main class="max-w-3xl mx-auto flex-grow p-8">
    </main>
    <footer class="py-4 text-center">
      Icons by <a href="https://fontawesome.com" target="_new">Font Awesome</a>.
      Source code on <a href="https://github.com/maryiskickass/mcb" target="_new">GitHub</a>.
    </footer>
  </div>
</template>

<script>
export default {
  name: 'app',
  data: () => ({
    socialLinks: [
      {
        icon: 'twitter',
        url: 'https://twitter.com/maryiskickass',
      },
      {
        icon: 'linkedin',
        url: 'https://linkedin.com/in/marycatherinebrannen',
      },
    ],
  }),
};
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Source+Sans+Pro:400,600&display=swap');

html, body {
  font-family: 'Source Sans Pro';
}

.bg-me {
  background: linear-gradient(rgba(0,0,0,0.4),rgba(0,0,0,1)), url('/images/mary.jpg');
}

footer a {
  @apply underline text-indigo-700;
}
</style>
