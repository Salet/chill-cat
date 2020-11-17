<template>
  <div class="cont">
    <Header />
    <Nuxt />
  </div>
</template>

<style>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  background: #e6f1f7;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

.cont {
  max-width: 1200px;
  margin: 20px auto;
}

h1,
h2,
h3,
h4,
h5,
h6 {
  @apply my-4;
}

h1 {
  @apply text-2xl;
}

h2 {
  @apply text-xl;
}

h3 {
  @apply text-lg;
}
</style>
