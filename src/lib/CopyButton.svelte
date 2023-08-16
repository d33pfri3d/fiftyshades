<script>
  export let text = "";

  async function copyToClipboard() {
    try {
      await navigator.clipboard.writeText(text);
      alert("Copied to clipboard");
    } catch (err) {
      console.error("Failed to copy text: ", err);
    }
  }
</script>

<button on:click={copyToClipboard}>Copy to Clipboard</button>

<style>
  /* Style your button as needed */
  button {
    padding: 10px 15px;
    cursor: pointer;
    border: none;
    background-color: #007bff;
    color: white;
    border-radius: 4px;
    font-size: 1rem;
    transition: background-color 0.3s;
  }

  button:hover {
    background-color: #0056b3;
  }
</style>
