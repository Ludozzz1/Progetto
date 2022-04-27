<script>
    export let list;
</script>

<div class="card has-background-dark  is-size-4 ml-3 ">
  <div class="card-content">
    <div class="content">
      <nav class="level">
         <div class='column box has-background-grey-dark has-text-light'>
           {#each list as el}
             <label class="checkbox">
                <input type="checkbox">
               {el}
             </label><br>
           {/each }
         </div>
      </nav>
    </div>
  </div>
</div>