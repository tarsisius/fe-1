<script lang="ts">
  import styles from '$lib/styles'
  import { assets } from '$lib/constants'
  import GetStarted from '$lib/components/get_started.svelte'
</script>

<section id="home" class="flex md:flex-row flex-col {styles.paddingY}">
  <div class="flex-1 {styles.flexStart} flex-col xl:px-0 sm:px-16 px-6">
    <div
      class="flex flex-row items-center py-[6px] px-4 bg-discount-gradient rounded-[10px] mb-2"
    >
      <img src={assets.discount} alt="discount" class="w-[32px] h-[32px]" />
      <p class="{styles.paragraph} ml-2">
        <span class="text-white">20%</span>
        Discount For {' '}
        <span class="text-white">1 Month</span>
        Account
      </p>
    </div>
    <div class="flex flex-row justify-between items-center w-full">
      <h1
        class="flex-1 font-poppins font-semibold ss:text-[72px] text-[52px] text-white ss:leading-[100px]"
      >
        The Next <br class="sm:block hidden" />
        {' '}
        <span class="text-gradient"> Generation </span>
      </h1>
      <div class="ss:flex hidden md:mr-4 mr-0">
        <GetStarted />
      </div>
    </div>
    <h1
      class="flex-1 font-poppins font-semibold ss:text-[68px] text-[52px] text-white ss:leading-[100px] w-full"
    >
      Payment Method.
    </h1>
    <p class="{styles.paragraph} max-w-[470px] mt-5">
      Our team of experts uses a methodolgy to identify the credit cards most
      likely to fit your needs. We examine annual percentage rates, annual fees.
    </p>
  </div>
  <div class="flex flex-1 {styles.flexCenter} md:my-0 my-10 relative">
    <img
      src={assets.robot}
      alt="billing"
      class="w-[100%] h-[100%] relative z-[5]"
    />
    <div class="absolute z-[0] w-[40%] h-[35%] top-0 pink__gradient" />
    <div
      class="absolute z-[0] w-[80%] h-[80%] rounded-full bottom-40 white_gradient"
    />
    <div
      class="absolute z-[0] w-[50%] h-[50%] right-20 bottom-20 blue__gradient"
    />
  </div>
  <div class="ss:hidden {styles.flexCenter}" />
</section>
