<script>
  let inputArray = ["General", "Onboarding", "Custom Domain", "Messaging"];
  let insertedValue = "";
  let inputField;
  function handleInput(e) {
    let value = e.target.value;
    insertedValue = value;
    insertedValue = insertedValue;
  }

  function handleAdd() {
    inputArray.push(insertedValue);
    inputArray = inputArray;
    inputField.value = "";
  }
</script>

<div class="container">
  <div class="input">
    <input bind:this={inputField} on:input={handleInput} type="text" />
    <button class="addBtn" on:click={handleAdd}>Add more Menu</button>
  </div>
  <div class="generatedComp">
    <h2>Settings</h2>
    {#if inputArray.length === 0}
      <h2>Nothing To Show... Add some links to see</h2>
    {:else}
      {#each inputArray as btnValue}
        <button class="generatedBtn">
          {btnValue}
        </button>
      {/each}
    {/if}
  </div>
</div>

<style>
  .container {
    margin: 2rem;
    width: 600px;
  }
  input {
    padding: 1rem 0.5rem;
    border: none;
    border-radius: 10px;
    width: 60%;
    font-size: 1.2rem;
  }
  .addBtn {
    font-size: 1rem;
    transition: all ease-in 0.2s;
    padding: 0.8rem;
    border: none;
    border-radius: 0 10px 0 10px;
    cursor: pointer;
    font-weight: bold;
    font-family: "Poppins", sans-serif;
  }
  .generatedComp {
    margin: 1rem;
  }
  .generatedBtn {
    font-size: 1.4rem;
    border-radius: 10px;
    border: none;
    margin: 10px 0;
    background: transparent;
    display: block;
    padding: 0.5rem 1rem;
    transition: all ease-in 0.2s;
  }
  .generatedBtn:hover,
  .addBtn:hover {
    background: black;
    color: white;
  }
</style>
