<template>
  <div>
    <h1>Chill Cat's gallery</h1>
    <div v-if="!$route.params.slug" class="flex">
      <NuxtLink v-for="pic in pictures" :key="pic.id" :to="`/gallery/${pic.id}`">
        <img :src="require(`~/assets/${pic.id}.jpg`)" class="thumb" alt="" />
        <p class="mt-2 text-sm">{{ pic.text }}</p>
      </NuxtLink>
    </div>

    <div v-if="$route.params.slug">
      <div class="flex justify-between text-sm mb-4">
        <NuxtLink to="/gallery">← Back to gallery</NuxtLink>
        <p>{{ pictures.find((pic) => pic.id == $route.params.slug).text }}</p>
      </div>
      <img :src="require(`~/assets/${$route.params.slug}.jpg`)" alt="" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      pictures: [
        { id: 1, text: 'Just chilling' },
        { id: 2, text: 'Showing his tail' },
        { id: 3, text: 'Enjoying himself as usual' },
        { id: 4, text: 'Being very pleased' },
      ],
    }
  },
}
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
