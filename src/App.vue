<script>
export default {
  name: 'App',
  data() {
    return {
      messagge: "This is a random image",
      url: "https://picsum.photos/400/300",
    }
  }
}
</script>

<template>
  <h1>{{ messagge }}</h1>
  <div>
    <img :src="url" alt="Photo Random">
  </div>
</template>

<style></style>
