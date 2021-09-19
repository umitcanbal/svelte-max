<script>
  let name = "ümitcan";
  let surname = "bal";
  let age = 29;

  $: upperCaseName = name.toUpperCase(); // pass by reference
  let upperCaseSurname = surname.toUpperCase(); // pass by value

  $: console.log(`upperCaseName`, upperCaseName); // logs everytime the value changes
  $: console.log(`upperCaseSurname`, upperCaseSurname); // logs only once

  const changeName = () => {
    name = "Ali";
  };

  const changeSurname = () => {
    surname = "Yılmaz";
  };

  const incrementAge = () => {
    age += 1;
  };

  $: if (age % 4 === 3) {
    // logs whenever the condition is met
    console.log(`age`, age);
  }
</script>

<h1>
  My name is {upperCaseName}, my surname is {upperCaseSurname}, my age is {age}
</h1>
<button on:click={changeName}>Change Name</button>
<button on:click={changeSurname}>Change Surname</button>
<button on:click={incrementAge}>Change Age</button>

<style>
  h1 {
    color: purple;
  }
</style>
