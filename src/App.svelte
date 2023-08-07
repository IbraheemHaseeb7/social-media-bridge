<script lang="ts">
  import Button from "./lib/Button.svelte";
  import FaLinkedin from "svelte-icons-pack/fa/FaBrandsLinkedin";
  import FaTwitter from "svelte-icons-pack/fa/FaBrandsTwitter";
  import Input from "./lib/Input.svelte";

  let connectedPlatforms: { name: string; status: boolean; icon: any }[] = [
    { name: "LinkedIn", status: false, icon: FaLinkedin },
    { name: "Twitter", status: false, icon: FaTwitter },
  ];
</script>

<main>
  <h1>Welcome Back</h1>
  <p>
    Write post here and it will publish it on all of your connected social media
    platforms
  </p>
  {#each connectedPlatforms as value}
    {#if value.status}
      <p style="color: green;">Already Connected to {value.name}</p>
    {:else}
      <Button text={`Connect to ${value.name}`} icon={value.icon} />
    {/if}
  {/each}
  <Input />
  <button>submit</button>
</main>

<style>
  main {
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    gap: 1rem;
  }

  h1,
  p {
    margin: 0;
  }
</style>
