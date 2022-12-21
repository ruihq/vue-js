<template>
    <div>
      <button @click="incrementLikes">Like</button>
      <span>{{ likes }}</span>
    </div>
</template>

<template>
    <div>
      <liking-component v-bind:likes="article.likes"></liking-component>
    </div>
  </template>
  
  <script>
  import LikingComponent from './LikingComponent.vue';
  
  export default {
    components: {
      LikingComponent
    },
    data() {
      return {
        article: {
          likes: 0
        }
      }
    }
  }
  </script>
