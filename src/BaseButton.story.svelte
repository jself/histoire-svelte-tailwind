<script>
  import { logEvent } from 'histoire/client'
  import BaseButton from './components/BaseButton.svelte'

  export let Hst

  let disabled = false
  let size = 'medium'
  let primary = false
</script>
  
<Hst.Story title="Buttons/BaseButton">
  <BaseButton {disabled} {primary} {size} on:click={event => logEvent('click', event)}>
    Click me!
  </BaseButton>
  <div style="margin-top: 6px;">
    <label>
      <input type="checkbox" bind:checked={disabled} >
      Disabled
    </label>
  </div>

  <svelte:fragment slot="controls">
    <Hst.Checkbox
      bind:value={disabled}
      title="Disabled"
    />
    <Hst.Select
      bind:value={size}
      options={['small', 'medium', 'large']}
      title="Size"
    />
    <Hst.Checkbox
      bind:value={primary}
      title="Primary"
    />
    <pre>{JSON.stringify({ disabled, size, primary }, null, 2)}</pre>
  </svelte:fragment>
</Hst.Story>

<style>
  pre {
    padding: 8px;
    background: rgba(0, 0, 0, .1);
    border-radius: 4px;
    margin: 8px;
    font-size: 0.8rem;
  }
</style>
