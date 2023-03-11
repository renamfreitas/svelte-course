<script>
  import Header from './UI/Header/Header.svelte'
  import MeetupItem from './Meetups/MeetupItem/MeetupItem.svelte'

  import { meetups } from './mockdata.js'

</script>

<style>
  #meetups {
    margin-top: 10rem;
  }
</style>

<Header />

<section id="meetups">

</section>
{#each meetups as meetup}
  <MeetupItem {meetup} />
{/each}