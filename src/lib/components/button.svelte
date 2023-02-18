<script lang="ts">
  import { features } from '$lib/constants'
  import Button from '$lib/components/button.svelte'

  export let styles: string | null = null
</script>

<button
  type="button"
  class="py-4 px-6 bg-blue-gradient font-poppins font-medium text-[18px] text-primary outline-none {styles}"
>
  Get Started
</button>
