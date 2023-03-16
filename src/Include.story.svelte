<script>
  import BaseButton from "./components/BaseButton.svelte"

  export let Hst
</script>

<Hst.Story title="Buttons/Multiple Buttons">
  <Hst.Variant title="all the buttons">
    <div class="flex gap-4 flex-col">
      <BaseButton size="small">Small</BaseButton>
      <BaseButton size="medium">Medium</BaseButton>
      <BaseButton size="large">Large</BaseButton>
      <BaseButton primary={true} size="small">Primary</BaseButton>
    </div>
  </Hst.Variant>
</Hst.Story>
