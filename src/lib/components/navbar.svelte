<script lang="ts">
  import { assets, navLinks } from '$lib/constants'
  const { close, logo, menu } = assets
  let toggle = false
</script>

<nav class="w-full flex py-6 justify-between items-center navbar">
  <img src={logo} alt="hoobank" class="w-[124px] h-[32px]" />
  <ul class="list-none sm:flex hidden justify-end items-center flex-1">
    {#each navLinks as nav, i}
      <li
        class="font-poppins font-normal cursor-pointer text-[16px] text-white {
          i === navLinks.length - 1 ? 'mr-0' : 'mr-10'
        }"
      >
        <a href="#{nav.id}">{nav.title}</a>
      </li>
    {/each}
  </ul>
  <div class="sm:hidden flex flex-1 justify-end items-center">
    <button on:click={() => (toggle = !toggle)}>
      <img
        src={toggle ? close : menu}
        alt="menu"
        class="w-[28px] h-[28px] object-contain"
      />
    </button>
    <div
      class="{
        toggle ? 'flex' : 'hidden'
      } p-6 bg-black-gradient absolute top-20 right-0 mx-4 my-2 min-w-[140px] rounded-xl sidebar"
    >
      <ul class="list-none justify-end items-center flex-1">
        {#each navLinks as nav, i}
          <li
            class="font-poppins font-normal cursor-pointer text-[16px] text-white {
              i === navLinks.length - 1 ? 'mb-0' : 'mb-4'
            }"
          >
            <a href="#{nav.id}">{nav.title}</a>
          </li>
        {/each}
      </ul>
    </div>
  </div>
</nav>
