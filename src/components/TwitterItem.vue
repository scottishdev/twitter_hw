<template lang="html">
  <div class="item-box">
    <h3>ID: {{item.id}}</h3>
    <h3>Name: {{item.name}}</h3>
    <h3>Handle: {{item.handle}}</h3>
    <img v-bind:src="item.img" alt="Twitter avatar" class="avatar">
    <h3>Tweet: {{item.tweet}}</h3>
    <h3>Likes: {{item.likes}}</h3>

    <!-- <form class="" action="index.html" method="post" v-on:submit.prevent="saveTweet">
      <label for="new-tweet">Tweet Something!</label>
      <input type="text" name="new-tweet" placeholder="Tweet Something!" v-model="">
      <input type="submit" value="Submit">
    </form> -->
  </div>
</template>

<script>
export default {
  name: 'twitter-item',
  props: ['item']

}
</script>

<style lang="css" scoped>
.avatar {
  width: 50px;
  height: 50px;
  border-radius: 50px;
}

.item-box {
  border-style: solid;
}

</style>
