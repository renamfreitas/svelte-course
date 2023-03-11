<script>
  export let id
  export let label
  export let rows
  export let value
  export let type = 'text'
</script>

<style lang="scss">
  @import "./TextInput.scss";
</style>

<div class="form-control">
  <label for={id}>{label}</label>
  {#if type === 'textarea'}
    <textarea rows={rows} id={id} value={value} on:input />
  {:else}
    <input type={type} id={id} value={value} on:input />
  {/if}
</div>