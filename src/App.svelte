<script>
  import Header from './UI/Header/Header.svelte'
  import MeetupGrid from './Meetups/MeetupGrid/MeetupGrid.svelte'

  import { meetups } from './mockdata.js'

</script>

<Header />

<MeetupGrid {meetups} />