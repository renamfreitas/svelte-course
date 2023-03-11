<script>
  import MeetupItem from "../MeetupItem/MeetupItem.svelte";

  export let meetups;

</script>

<style lang="scss">
  @import "./MeetupGrid.scss";
</style>

<section id="meetups">
  {#each meetups as meetup}
    <MeetupItem {meetup} />
  {/each}
</section>