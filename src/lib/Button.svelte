<script lang="ts">
  import Icon from "svelte-icons-pack/Icon.svelte";

  export let text: string;
  export let icon;
</script>

<button>
  {text}

  <Icon src={icon} size="25" color="#fff" />
</button>

<style>
    button {
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        gap: 0.5rem;
    }
</style>