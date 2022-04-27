<script>
  let RArticle
</script>

<article bind:this={RArticle} class="message is-dark is-size-5 ml-6 mr-6">
    <div class="message-header">
      <button class="delete" on:click={RArticle.remove()} aria-label="delete"></button>
    </div>
    <div class="message-body">
        This tool strives to give the users the chance to develop their own geoid at nations' borders, created from eligeble geoids chosen on the base of the information provided by the users themselves.
    </div>
</article>   