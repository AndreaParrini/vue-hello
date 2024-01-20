<script>
export default {
  name: 'App',
  data() {
    return {
      messagge: "",
      url: "https://picsum.photos/400/300",
      background: "",
      title: "",
    }
  },
  methods: {
    modifyBackground() {
      this.background = "background-red";
    },
    addTitle() {
      this.title = this.messagge
    }
  }
}
</script>

<template>
  <input type="text" v-model="messagge" placeholder="Insert HERE the title of page and then press 'Enter'"
    @keyup.enter="addTitle">
  <h1 v-bind:class="background">{{ title }}</h1>
  <div>
    <img :src="url" alt="Photo Random">
  </div>
  <div>
    <button v-on:click="modifyBackground">Add red background to title</button>
  </div>
</template>

<style>
.background-red {
  background: red;
}

input {
  width: 100%;
}
</style>
