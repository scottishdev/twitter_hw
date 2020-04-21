<template lang="html">
  <div>
    <h3>ID: {{item.id}}</h3>
    <h3>Name: {{item.name}}</h3>
    <h3>Handle: {{item.handle}}</h3>
    <img v-bind:src="item.img" alt="Twitter avatar" class="avatar">
    <h3>Tweet: {{item.tweet}}</h3>
    <h3>Likes: {{item.likes}}</h3>
  </div>
</template>

<script>
export default {
  name: 'twitter-item',
  props: ['item'],
}
</script>

<style lang="css" scoped>
.avatar {
  width: 50px;
  height: 50px;
  border-radius: 50px;
}

</style>
