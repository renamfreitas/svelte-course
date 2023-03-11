<script>
  import Header from './UI/Header/Header.svelte'
  import MeetupGrid from './Meetups/MeetupGrid/MeetupGrid.svelte'
  import TextInput from './UI/TextInput/TextInput.svelte';

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

<style>
  form {
    width: 30rem;
    max-width: 90%;
    margin: auto;
  }
</style>

<Header />

<main>
  <form on:submit|preventDefault={addMeetup}>
    <TextInput 
      id="title"
      label="Title"
      value={title}
      on:input={event => (title = event.target.value)} 
    />
    <TextInput 
      id="subtitle"
      label="Subtitle"
      value={subtitle}
      on:input={event => (subtitle = event.target.value)} 
    />
    <TextInput 
      id="address"
      label="Address"
      value={address}
      on:input={event => (address = event.target.value)} 
    />
    <TextInput 
      id="imageUrl"
      label="Image URL"
      value={imageUrl}
      on:input={event => (imageUrl = event.target.value)} 
    />
    <TextInput 
      id="email"
      label="E-mail"
      value={email}
      type="email"
      on:input={event => (email = event.target.value)} 
    />
    <TextInput 
      id="description"
      label="Description"
      type="textarea"
      rows="3"
      value={description}
      on:input={event => (description = event.target.value)} 
    />
    <button type="submit">Save</button>
  </form>
  <MeetupGrid {meetups} />
</main>
