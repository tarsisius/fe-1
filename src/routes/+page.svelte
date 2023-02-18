<script lang="ts">
  import styles from '$lib/styles'

  import Billing from '$lib/components/billing.svelte'
  import Bussiness from '$lib/components/bussiness.svelte'
  import CardDeal from '$lib/components/card_deal.svelte'
  import Clients from '$lib/components/clients.svelte'
  import Cta from '$lib/components/cta.svelte'
  import Footer from '$lib/components/footer.svelte'
  import Hero from '$lib/components/hero.svelte'
  import Navbar from '$lib/components/navbar.svelte'
  import Stats from '$lib/components/stats.svelte'
  import Testimonials from '$lib/components/testimonials.svelte'
</script>

<div class="bg-primary w-full overflow-hidden">
  <div class={`${styles.paddingX} ${styles.flexCenter}`}>
    <div class={`${styles.boxWidth}`}>
      <Navbar />
    </div>
  </div>

  <div class={`bg-primary ${styles.flexStart}`}>
    <div class={`${styles.boxWidth}`}>
      <Hero />
    </div>
  </div>
  <div class={`bg-primary ${styles.paddingX} ${styles.flexStart}`}>
    <div class={`${styles.boxWidth}`}>
      <Stats />
      <Bussiness />
      <Billing />
      <CardDeal />
      <Testimonials />
      <Clients />
      <Cta />
      <Footer />
    </div>
  </div>
</div>
