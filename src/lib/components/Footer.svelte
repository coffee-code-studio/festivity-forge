<script lang="ts">
  import festivityForgeLogo from '$lib/assets/festivity-forge-logo-alt.png'
</script>

<footer class="bg-rose-50">
  <div class="mx-auto max-w-5xl px-4 py-16 sm:px-6 lg:px-8">
    <div class="flex justify-center text-green-600">
      <img src={festivityForgeLogo} width={120} height={120} alt="Terra Tint" />
    </div>

    <div class="flex justify-center text-rose-800">
      Designed by&nbsp;<a href="https://coffeecodestudio.com/"><strong class="bg-gradient-to-r from-green-300 via-blue-500 to-purple-600 bg-clip-text text-transparent">Coffee Code Studio</strong></a>
    </div>

    <ul class="mt-12 flex flex-wrap justify-center gap-6 md:gap-8 lg:gap-12">
      <li>
        <a class="text-rose-800 transition hover:text-rose-800" href="/about">Home</a>
      </li>
      <li>
        <a class="text-rose-800 transition hover:text-rose-800" href="/about">About</a>
      </li>
      <li>
        <a class="text-rose-800 transition hover:text-rose-800" href="/contact">Contact</a>
      </li>
    </ul>
  </div>
</footer>
