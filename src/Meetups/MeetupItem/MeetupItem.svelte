<script>
  export let meetup

  let {title, subtitle, address, imageUrl, description, email} = meetup
</script>

<style lang="scss">
  @import "./MeetupItem.scss";
</style>

<article>
  <header>
    <h1>{title}</h1>
    <h2>{subtitle}</h2>
    <p>{address}</p>
  </header>
  <div class="image">
    <img src="{imageUrl}" alt="{title}">
  </div>
  <div class="content">
    <p>{description}</p>
  </div>
  <footer>
    <a href="mailto:{email}">Contact</a>
    <button>Show details</button>
    <button>Favorite</button>
  </footer>
</article>