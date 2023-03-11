<script>
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
    <a href="mailto:{meetup.email}">Contact</a>
    <button>Show details</button>
    <button>Favorite</button>
  </footer>
</article>