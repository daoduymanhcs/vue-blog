<template>
  <li>
    <div class="post">
      <a v-bind:href="post.url" target="_blank" class="thumbnail" style="background-image: url(&quot;https://b.thumbs.redditmedia.com/-yFxggVsM18wNDPgokvgbz68QzPI-oHDs7tKFn1VQew.jpg&quot;);"></a>
       <div class="details"><a href="https://i.redd.it/1i6ovy5jrhlz.gif" title="happy lil bird knows how cute she is" target="_blank" class="title">
         {{ post.title }}</a>
         <div class="action-buttons">
           <a href="" title="Vote"><i class="material-icons">thumbs_up_down</i>
             59027
           </a>
           <a href="" title="Go to discussion"><i class="material-icons">forum</i>
             874
           </a>
         </div>
       </div>
     </div>
  </li>
</template>

<script>
  export default {
    props: {
      post: {
        required: true
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
