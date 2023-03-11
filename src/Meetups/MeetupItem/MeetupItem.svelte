<script>
  import Button from "../../UI/Button/Button.svelte";

  export let meetup

</script>

<style lang="scss">
  @import "./MeetupItem.scss";
</style>

<article>
  <header>
    <h1>{meetup.title}</h1>
    <h2>{meetup.subtitle}</h2>
    <p>{meetup.address}</p>
  </header>
  <div class="image">
    <img src="{meetup.imageUrl}" alt="{meetup.title}">
  </div>
  <div class="content">
    <p>{meetup.description}</p>
  </div>
  <footer>
    <Button style="outline" href="mailto:{meetup.email}" caption="Contact" />
    <Button type="button" caption="Show details" />
    <Button type="button" caption="Favorite" />
  </footer>
</article>