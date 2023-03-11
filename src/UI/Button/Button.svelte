<script>
  export let type
  export let caption
  export let href
  export let style
</script>

<style lang="scss">
  @import "./Button.scss";
</style>

{#if href}
  <a class={style} {href}>{caption}</a>
{:else}
  <button class={style} type={type}>{caption}</button>
{/if}