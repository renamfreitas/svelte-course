<script>
  import Header from './UI/Header/Header.svelte'
  import MeetupGrid from './Meetups/MeetupGrid/MeetupGrid.svelte'

  import { meetups as mockData } from './mockdata.js'

  let meetups = mockData

  let title = ''
  let subtitle = ''
  let address = ''
  let email = ''
  let description = ''
  let imageUrl = ''
  

  function addMeetup() {
    const newMeetup = {
      id: Math.random().toString(),
      title: title,
      subtitle: subtitle,
      address: address,
      email: email,
      description: description,
      imageUrl: imageUrl
    }

    meetups = [newMeetup, ...meetups];
  }
</script>

<Header />

<main>
  <form on:submit|preventDefault={addMeetup}>
    <div class="form-control">
      <label for="title">Title</label>
      <input type="text" id="title" bind:value={title}>
    </div>
    <div class="form-control">
      <label for="subtitle">Subtitle</label>
      <input type="text" id="subtitle" bind:value={subtitle}>
    </div>
    <div class="form-control">
      <label for="address">Address</label>
      <input type="text" id="address" bind:value={address}>
    </div>
    <div class="form-control">
      <label for="imageUrl">Image Url</label>
      <input type="text" id="imageUrl" bind:value={imageUrl}>
    </div>
    <div class="form-control">
      <label for="email">E-mail</label>
      <input type="email" id="email" bind:value={email}>
    </div>
    <div class="form-control">
      <label for="description">Description</label>
      <textarea rows="3" id="description" bind:value={description} />
    </div>
    <button type="submit">Save</button>
  </form>
  <MeetupGrid {meetups} />
</main>
