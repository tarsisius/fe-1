<script lang="ts">
  import styles from '$lib/styles'
  import { clients } from '$lib/constants'
</script>

<section class="{styles.flexCenter} my-4">
  <div class="{styles.flexCenter} flex-wrap w-full">
    {#each clients as client}
      <div
        class="flex-1 {styles.flexCenter} sm:min-w-[192px] min-w-[120px] m-5"
      >
        <img
          src={client.logo}
          alt="client_logo"
          class="sm:w-[192px] w-[100px] object-contain"
        />
      </div>
    {/each}
  </div>
</section>
