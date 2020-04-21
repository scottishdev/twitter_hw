<template lang="html">
  <div class="">


  <h1>Twitter</h1>
  <h3>ID: {{tweet.id}}</h3>
  <h3>Name: {{tweet.name}}</h3>
  <h3>Handle: {{tweet.handle}}</h3>
  <h3>Image: {{tweet.image}}</h3>
  <h3>Tweet: {{tweet.tweet}}</h3>
  <h3>Likes: {{tweet.likes}}</h3>

  <h2>Total Likes: {{totalLikes}}</h2>
  
    </div>
</template>

<script>
export default {
  name: 'twitter-item',
  props: ['item']
}
</script>

<style lang="css" scoped>
</style>
