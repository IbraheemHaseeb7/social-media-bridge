<script lang="ts">
  let text: string = "";

  /**
   *
   * this function controlls the input that is typed so we
   * can perform little operations like how many characters
   * have been typed so far.
   *
   * @param {any} e
   */
  function handleChange(e: any) {
    e.preventDefault();

    text = e.target.value;
  }
</script>

<div>
  <textarea value={text} on:input={(e) => handleChange(e)} />
  <span>Count: {text.length}</span>
</div>

<style>
  div {
    width: 100%;
    position: relative;
  }
  textarea {
    width: 100%;
    height: 20rem;
    resize: vertical;
    background-color: transparent;
    border-radius: 8px;
    color: #fff;
    font-size: 15px;
    padding: 1rem;
    font-family: Inter, system-ui, Avenir, Helvetica, Arial, sans-serif;
  }
  span {
    font-size: 12px;
    color: #ffffff2c;
    position: absolute;
    bottom: 1rem;
    left: calc(100% - 5rem);
  }
</style>
