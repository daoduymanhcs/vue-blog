<template>
  <div class="subreddit">
    <h2>{{ name }}</h2>
    <ul class="item-list">
      <Detail v-for="post in posts" :post="post.data"></Detail>
    </ul>
  </div>
</template>

<script>
  import Detail from '@/components/Content/Detail'
  export default {
    data () {
      return {
        posts: null
      }
    },
    props: {
      name: {
        type: String,
        required: true
      }
    },
    computed: {
      getPost () {
        return this.posts
      }
    },
    created: function () {
      // `this` points to the vm instance
      this.axios.get('https://www.reddit.com/r/' + this.name + '/top.json?limit=5').then((response) => {
        this.posts = response.data.data.children
      })
    },
    components: {
      Detail
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
