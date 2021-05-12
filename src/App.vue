<template>
  <div class="flex flex-col min-h-screen text-xl">
    <header class="text-center px-5 py-24">
      <img class="inline-block w-48 h-48" src="/mcb/images/mary.jpg"/>
      <h1 class="mt-8 text-4xl font-semibold">Hello! I am Mary.</h1>
      <p class="mt-4 mb-8">I am a digital media professional currently based in Barcelona, Spain.</p>
      <p class="mt-4 mb-8">I leverage my 12+ years of online advertising experience to help companies of all sizes maximize their revenue.</p>
      <p class="mt-4 mb-8">I'm passionate about integrity, equality and diversity - and how a focus on purposeful inclusion in the workplace will bring success for both employers and employees.</p>
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
    <hr/>
    <main class="w-full mx-auto flex-grow p-8 grid grid-flow-row grid-cols-2">
      <section>
        <h2 class="text-3xl">Articles</h2>
        <ul class="ml-4 list-disc">
          <li v-for="article in articles">{{ article.title }}</li>
        </ul>
      </section>
      <section>
        <h2 class="text-3xl">Links</h2>
        <ul class="ml-4 list-disc">
          <li v-for="link in links">
            <a class="text-blue-700 underline" :href="link.url">
              {{ link.title }}
            </a>
          </li>
        </ul>
      </section>
    </main>
    <hr/>
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
    articles: [
      {
        title: 'My First Article',
      },
    ],
    links: [
      {
        title: 'Cool Website',
        url: 'https://iamdan.me/',
      },
    ],
    socialLinks: [
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
