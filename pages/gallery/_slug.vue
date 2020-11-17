<template>
  <div>
    <h1>Chill Cat's gallery</h1>
    <div v-if="!$route.params.slug">
      <NuxtLink to="/gallery/1"
        ><img src="~/assets/1.jpg" class="thumb" alt=""
      /></NuxtLink>
      <NuxtLink to="/gallery/2"
        ><img src="~/assets/2.jpg" class="thumb" alt=""
      /></NuxtLink>
      <NuxtLink to="/gallery/3"
        ><img src="~/assets/3.jpg" class="thumb" alt=""
      /></NuxtLink>
      <NuxtLink to="/gallery/4"
        ><img src="~/assets/4.jpg" class="thumb" alt=""
      /></NuxtLink>
    </div>
    <div v-if="$route.params.slug">
      <NuxtLink to="/gallery" class="text-sm mb-4 block"
        >← Back to gallery</NuxtLink
      >
      <img :src="require(`~/assets/${$route.params.slug}.jpg`)" alt="" />
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
img {
  @apply rounded-xl inline-block;
}

.thumb {
  @apply mr-4;
  height: 250px;
}
</style>
