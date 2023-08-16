<script>
  export let text = "";

  async function copyToClipboard() {
    try {
      await navigator.clipboard.writeText(text);
      alert(`Copied ${text} clipboard`);
    } catch (err) {
      console.error("Failed to copy text: ", err);
      alert("Failed to copy text");
    }
  }
</script>

<button on:click={copyToClipboard}>copy hex ✂️</button>

<style>
  /* Style your button as needed */
  button {
    cursor: pointer;
    border: 1px solid #1e1e1e;
    background-color: transparent;
    border-radius: 4px;
    padding: 0.5rem;
    font-size: 0.8rem;
    color: black;
  }

  button:hover {
    background-color: #9e9e9e;
  }
</style>
