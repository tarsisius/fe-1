<script lang="ts">
  import styles from '$lib/styles'
  import { assets } from '$lib/constants'
</script>

<div
  class="{styles.flexCenter} w-[140px] h-[140px] rounded-full bg-blue-gradient p-[2px] cursor-pointer"
>
  <div
    class="{styles.flexCenter} flex-col bg-primary w-[100%] h-[100%] rounded-full"
  >
    <div class="{styles.flexStart} flex-row">
      <p class="font-poppins font-medium text-[18px] leading-[23px] mr-2">
        <span class="text-gradient">Get</span>
      </p>
      <img
        src={assets.arrowUp}
        class="w-[23px] h-[23px] object-contain"
        alt="up"
      />
    </div>
    <p class="font-poppins font-medium text-[18px] leading-[23px]">
      <span class="text-gradient">Started</span>
    </p>
  </div>
</div>
