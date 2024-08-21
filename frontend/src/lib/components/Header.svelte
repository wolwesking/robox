<script>
  let menuOpen = false;

  function toggleMenu() {
    menuOpen = !menuOpen;
  }

  function closeMenu() {
    menuOpen = false;
  }
</script>

<header class="fixed top-0 left-0 right-0 bg-gradient-to-r from-gray-900 via-purple-700 to-gray-800 shadow-md z-50">
  <nav
    class="mx-auto flex max-w-7xl items-center justify-between p-6 lg:px-8 text-white"
    aria-label="Global"
  >
    <div class="flex lg:flex-1">
      <a href="/" class="-m-1.5 p-1.5">
        <span class="sr-only">BLXearn</span>
        <img class="h-8 w-auto" src="/logo.jpeg" alt="" />
      </a>
    </div>
    <div class="flex lg:hidden">
      <button
        type="button"
        class="-m-2.5 inline-flex items-center justify-center rounded-md p-2.5 text-gray-200"
        on:click={toggleMenu}
        aria-expanded={menuOpen ? 'true' : 'false'}
        aria-controls="mobile-menu"
      >
        <span class="sr-only">Open main menu</span>
        <svg
          class="h-6 w-6"
          fill="none"
          viewBox="0 0 24 24"
          stroke-width="1.5"
          stroke="currentColor"
          aria-hidden="true"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
          />
        </svg>
      </button>
    </div>
    <div class="hidden lg:flex lg:gap-x-12">
      <a
        href="/login"
        class="text-sm font-semibold leading-6 text-gray-200"
      >Earn</a>
      <a
        href="/login"
        class="text-sm font-semibold leading-6 text-gray-200"
      >Cashout</a>
      <a
        href="#frq"
        class="text-sm font-semibold leading-6 text-gray-200"
      >FRQ</a>
    </div>
    <div class="hidden lg:flex lg:flex-1 lg:justify-end">
      <button
        class="bg-purple-600 text-sm font-bold py-2 px-4 rounded text-white hover:bg-purple-700 focus:outline-none focus:ring-2 focus:ring-purple-500 focus:ring-opacity-50"
      >
        Log in <span aria-hidden="true">&rarr;</span>
      </button>
    </div>
  </nav>

  {#if menuOpen}
    <div id="mobile-menu" class="lg:hidden" role="dialog" aria-modal="true">
      <div
        class="fixed inset-0 z-10 bg-black opacity-50"
        role="button"
        tabindex="0"
        aria-label="Close menu"
        on:click={closeMenu}
        on:keydown={(event) => {
          if (event.key === 'Enter' || event.key === ' ') closeMenu();
        }}
      ></div>
      <div
        class="fixed inset-y-0 right-0 z-10 w-full overflow-y-auto bg-gradient-to-r from-purple-900 via-purple-800 to-purple-700 px-6 py-6 sm:max-w-sm sm:ring-1 sm:ring-gray-900/10"
      >
        <div class="flex items-center justify-between">
          <a href="/" class="-m-1.5 p-1.5">
            <span class="sr-only">BLXearn</span>
            <img class="h-8 w-auto" src="/logo.jpeg" alt="" />
          </a>
          <button
            type="button"
            class="-m-2.5 rounded-md p-2.5 text-gray-200"
            on:click={closeMenu}
            aria-label="Close menu"
          >
            <span class="sr-only">Close menu</span>
            <svg
              class="h-6 w-6"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              aria-hidden="true"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M6 18L18 6M6 6l12 12"
              />
            </svg>
          </button>
        </div>
        <div class="mt-6 flow-root">
          <div class="-my-6 divide-y divide-gray-500/10">
            <div class="space-y-2 py-6">
              <a
                href="/login"
                class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50"
                >Features</a>
              <a
                href="/login"
                class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50"
                >Marketplace</a>
              <a
                href="#frq"
                class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50"
                >Company</a>
            </div>
            <div class="py-6">
              <a
                href="/login"
                class="-mx-3 block rounded-lg px-3 py-2.5 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50"
                >Log in</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  {/if}
</header>
