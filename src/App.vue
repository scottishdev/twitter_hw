<template lang="html">
  <div>
    <h1>Twitter</h1>
    <ul>
      <twitter-item v-for="(item, index) in tweets" :key="index" :item="item"></twitter-item>
    </ul>
    <h3>Total Likes: {{totalLikes}}</h3>
  </div>
</template>

<script>

import TwitterItem from './components/TwitterItem.vue';

export default {
  name: 'app',
  data() {
    return {
      tweets:[
        {
          id: 1,
          name: 'James',
          handle: '@jokerjames',
          img: 'https://semantic-ui.com/images/avatar2/large/matthew.png',
          tweet: "If you don't succeed, dust yourself off and try again.",
          likes: 10,
        },
        {
          id: 2,
          name: 'Fatima',
          handle: '@fantasticfatima',
          img: 'https://semantic-ui.com/images/avatar2/large/molly.png',
          tweet: 'Better late than never but never late is better.',
          likes: 12,
        },
        {
          id: 3,
          name: 'Xin',
          handle: '@xeroxin',
          img: 'https://semantic-ui.com/images/avatar2/large/elyse.png',
          tweet: 'Beauty in the struggle, ugliness in the success.',
          likes: 18,
        }
      ]
    }
  },
  components: {
    'twitter-item': TwitterItem
  },
  computed: {
    totalLikes: function(){
      return this.tweets.reduce((accumulator, item) => {
        return accumulator + item.likes;
      }, 0);
    }
  }
}
</script>

<style lang="css" scoped>
</style>
