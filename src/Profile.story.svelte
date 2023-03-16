<script>
export let Hst
import Button from "./components/BaseButton.svelte"
const buttons = [
  {"text": "Hello"},
  {"text": "Hello2"},
  {"text": "Hello3"},
  {"text": "Hello4", "primary": true},
]
</script>

<Hst.Story title="A profile component">
  <!-- a profile component in tailwind -->
  <div class="flex">Hello Josh</div>
  {#each buttons as button}
    <Button primary={button.primary || false}>{button.text}</Button>
  {/each}
</Hst.Story>
