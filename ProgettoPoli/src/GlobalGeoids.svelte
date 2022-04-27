<script>
  export let global_selected = null
  let radio_1
  let radio_2
  let radio_3
  let passo = null
  export const passo_max = 100
  export const passo_min = 0

  function radioGeoide(params) {
    if(!global_selected){
      global_selected = radio_1
    }
    global_selected.classList.remove('is-primary',"is-medium","is-light")
    params.target.classList.add('is-primary',"is-medium",'is-light')
    global_selected = params.target
  }
</script>

<div class="card has-background-dark has-text-light is-size-4 ml-6 mr-6">
  <div class="card-content">
    <div class="content">
      <div class="columns pr-6">
        <div class="column level">
          <div class="level-item">
            <div class="field is-grouped">
              <p class="control">
                <button bind:this={radio_1} class="button" on:click={radioGeoide}>Primo geoide</button>
              </p>
              <p class="control">
                <button bind:this={radio_2} class="button" on:click={radioGeoide}>Secondo geoide</button>
              </p>
              <p class="control">
                <button bind:this={radio_3} class="button" on:click={radioGeoide}>Terzo geoide</button>
              </p>
            </div> 
          </div>
        </div>
        <div class="column is-two-fifths">
          <input class="input" type="number" bind:value={passo} max={passo_max} min={passo_min} step="1">
          <p class="help is-light">Se il passo non viene specificato, esso verrà scelto automaticamente; il range del passo è da {passo_min} a {passo_max}</p>
        </div>
      </div>
    </div>
  </div>
</div>

