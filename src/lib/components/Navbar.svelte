<script lang="ts">
  import { onMount, onDestroy } from 'svelte'
  import festivityForgeLogo from '$lib/assets/festivity-forge-logo-alt.png'
  import styles from '../../nav.module.css'

  let isMenuOpen = false

  function toggleMenu() {
    isMenuOpen = !isMenuOpen
  }

  function handleKeydown(event: KeyboardEvent): void {
    if (event.key === 'Enter' || event.key === ' ') {
      toggleMenu()
    }
  }

  onMount(() => {
    const handleHashChange = () => {
      isMenuOpen = false
    }
    
    window.addEventListener('hashchange', handleHashChange)

    onDestroy(() => {
      window.removeEventListener('hashchange', handleHashChange)
    })
  })
</script>

<nav class="bg-rose-50">
  <div class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto p-4">
    <a href="/" class="flex items-center space-x-3 rtl:space-x-reverse">
        <img src={festivityForgeLogo} width={80} height={80} alt="Festivity Forge" />
    </a>
    <button on:click={toggleMenu} class="inline-flex items-center p-2 w-10 h-10 justify-center text-sm text-white rounded-lg md:hidden focus:outline-none focus:ring-2 bg-rose-200" aria-controls="navbar-default" aria-expanded={isMenuOpen}>
      <span class="sr-only">Open main menu</span>
      <!-- Hamburger Icon -->
      <svg class="w-5 h-5" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 17 14">
        <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 1h15M1 7h15M1 13h15"/>
      </svg>
    </button>
    <!-- Desktop Nav Links -->
    <div class="hidden w-full md:block md:w-auto" id="navbar-default">
      <ul class="font-medium flex flex-col p-4 md:p-0 mt-4 rounded-lg md:flex-row md:space-x-8 rtl:space-x-reverse md:mt-0 md:border-0">
        <li>
          <a href="/" class="block py-2 px-3 text-rose-800 rounded md:bg-transparent md:text-rose-800 md:p-0" aria-current="page">Home</a>
        </li>
        <li>
          <a href="/about" class="block py-2 px-3 text-rose-800 rounded md:bg-transparent md:text-rose-800 md:p-0">About</a>
        </li>
        <li>
          <a href="/contact" class="block py-2 px-3 text-rose-800 rounded md:bg-transparent md:text-rose-800 md:p-0">Contact</a>
        </li>
      </ul>
    </div>
  </div>

  <!-- Backdrop -->
  <div class={`fixed inset-0 z-20 ${isMenuOpen ? 'bg-black opacity-50' : 'opacity-0 pointer-events-none'} transition-opacity duration-300 ease-in-out`} on:click={toggleMenu} on:keydown={handleKeydown} role="button" aria-pressed={isMenuOpen ? 'true' : 'false'} tabindex="0"></div>
  
  <!-- Full screen menu for mobile -->
  <div class={`fixed inset-0 z-30 ${isMenuOpen ? styles.menuEnterActive : styles.menuExitActive} transform transition-transform duration-300 ease-in-out bg-rose-50`}>
    <div class="flex flex-col h-full">
      <!-- Close Button -->
      <button class="self-end p-4" on:click={toggleMenu}>
        <svg class="w-6 h-6 text-rose-800" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>
      <!-- Menu Items -->
      <ul class="flex-grow flex flex-col items-center justify-center">
        <li>
          <a on:click={toggleMenu} href="/" class="block text-lg py-2 px-3 text-rose-800 rounded md:p-0" aria-current="page">Home</a>
        </li>
        <li>
          <a on:click={toggleMenu} href="/about" class="block text-lg py-2 px-3 text-rose-800 rounded md:p-0">About</a>
        </li>
        <li>
          <a on:click={toggleMenu} href="/contact" class="block text-lg py-2 px-3 text-rose-800 rounded md:p-0">Contact</a>
        </li>
      </ul>
    </div>
  </div>
</nav>
