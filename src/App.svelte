<script>
  import axios from "axios";
  import { onMount } from "svelte";

  $: time = "loading...";

  onMount(() => {
    axios.get("/api").then(res => {
      setTimeout(() => {
        time = res.data.time;
      }, 1000);
    });
  });
</script>

<style>
  h1 {
    color: purple;
  }
</style>

<h1>PRODUCTION: The time is currently: {time}</h1>
