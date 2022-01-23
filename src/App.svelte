<script>
  import Header from "./UI/Header.svelte";
  import MeetupItem from "./Meetups/MeetupItem.svelte";

  const meetups = [
    {
      id: "m1",
      title: "Title1",
      subtitle: "Subtitle1",
      description: "Description1",
      imageURL:
        "https://i.picsum.photos/id/10/2500/1667.jpg?hmac=J04WWC_ebchx3WwzbM-Z4_KC_LeLBWr5LZMaAkWkF68",
      address: "Address1",
      contact: "email1@test.com",
    },
    {
      id: "m2",
      title: "Title2",
      subtitle: "Subtitle2",
      description: "Description2",
      imageURL:
        "https://i.picsum.photos/id/100/2500/1656.jpg?hmac=gWyN-7ZB32rkAjMhKXQgdHOIBRHyTSgzuOK6U0vXb1w",
      address: "Address2",
      contact: "email2@test.com",
    },
  ];
</script>

<Header />

<section id="meetups">
  {#each meetups as meetup}
    <MeetupItem />
  {/each}
</section>

<style>
  #meetups {
    margin-top: 5rem;
  }
</style>
