<script lang="ts">
  import styles, { layout } from '$lib/styles'
  import { features } from '$lib/constants'
  import Button from '$lib/components/button.svelte'
</script>

<section id="features" class={layout.section}>
  <div class={layout.sectionInfo}>
    <h2 class={styles.heading2}>
      You do the bussines, <br class="sm:block hidden" /> we'll handle the money.
    </h2>
    <p class="{styles.paragraph} max-w-[470px] mt-5">
      With the right credit card, you can improve your financial life by
      building credit, earning rewards and saving money. But with hundreds of
      credit cards on the market.
    </p>
    <Button styles="mt-10" />
  </div>
  <div class="{layout.sectionImg} flex-col">
    {#each features as feature, i}
      <div
        class='flex flex-row p-6 rounded-[20px] {
          i !== features.length - 1 ? 'mb-6' : 'mb-0'
        } feature-card'
      >
        <div
          class='w-[64px] h-[64px] rounded-full {styles.flexCenter} bg-dimBlue'
        >
          <img
            src={feature.icon}
            alt="star"
            class="w-[50%] h-[50%] object-contain"
          />
        </div>
        <div class="flex-1 flex flex-col ml-3">
          <h4
            class="font-poppins font-semibold text-white text-[18px] leading-[23.4px] mb-1"
          >
            {feature.title}
          </h4>
          <p
            class="font-poppins font-normal text-dimWhite text-[16px] leading-[24px]"
          >
            {feature.content}
          </p>
        </div>
      </div>
    {/each}
  </div>
</section>
