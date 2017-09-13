<template>
  <div id="main">
    <div class="container">
      <Post name="gifts"></Post>
      <Post name="games"></Post>
      <Post name="holidays"></Post>
      <Post name="computers"></Post>
      <Post name="cups"></Post>
      <Post name="cakes"></Post>
    </div>
  </div>
</template>

<script>
import Post from '@/components/Content/Post'
export default {
  components: {
    Post
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
