<script lang="ts">
  export let disabled: boolean = false
  export let size: 'small' | 'medium' | 'large' = 'medium'
  export let primary: boolean = false
</script>

<button class={`rounded-lg ${primary ? 'primary' : 'secondary'} ${size}`} class:disabled={disabled}>
  <slot />
</button>

<style>
.primary {
  @apply bg-green-500;
}
.secondary {
  @apply bg-gray-500;
}

.disabled {
  @apply bg-opacity-50 cursor-not-allowed;
}

.small {
  @apply p-1 text-sm;
}

.medium {
  @apply p-2 text-lg;
}

.large {
  @apply p-4 text-xl;
}
</style>
