<script>
  // import { onDestroy, onMount } from "svelte";

  import PollStore from "../stores/PollStore";
  import PollDetails from "./PollDetails.svelte";
  // export let polls = [];

  // const unsub = PollStore.subscribe((data) => {
  //   polls = data;
  // });

  // onDestroy(() => {
  //   unsub();
  // });
</script>

<div class="poll-list">
  {#each $PollStore as poll (poll.id)}
    <div>
      <PollDetails {poll} />
    </div>
  {/each}
</div>

<!-- markup (zero or more items) goes here -->
<style>
  .poll-list {
    margin: 0 40px;
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 20px;
  }
</style>
