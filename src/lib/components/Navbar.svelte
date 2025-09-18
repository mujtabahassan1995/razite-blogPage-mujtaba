<script>
  let isOpen = false;
</script>

<nav class="bg-white shadow-md">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="gap-[70%] flex justify-between h-16 items-center">
      
      <!-- Logo -->
      <div class="flex-shrink-0 text-2xl font-bold text-green-700">
        <a href="/">MySite</a>
      </div>

      <!-- Desktop Menu -->
      <div class="hidden sm:w-full sm:flex space-x-8">
        <a href="/" class="text-gray-700 hover:text-green-700 font-medium">Home</a>
        <a href="/blog" class="text-gray-700 hover:text-green-700 font-medium">Blog</a>
        <a href="/contact" class="text-gray-700 hover:text-green-700 font-medium">Contact</a>
      </div>

      <!-- Mobile Menu Button -->
      <div class="sm:hidden">
        <button 
          class="text-gray-700 hover:text-green-700 focus:outline-none"
          on:click={() => isOpen = !isOpen}
        >
          <!-- Hamburger Icon -->
          <svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" 
              d="M4 6h16M4 12h16M4 18h16" />
          </svg>
        </button>
      </div>
    </div>
  </div>

  <!-- Mobile Dropdown -->
  {#if isOpen}
    <div class="sm:hidden bg-white shadow-md">
      <a href="/" class="block px-4 py-2 text-gray-700 hover:bg-gray-100">Home</a>
      <a href="/blog" class="block px-4 py-2 text-gray-700 hover:bg-gray-100">Blog</a>
      <a href="/contact" class="block px-4 py-2 text-gray-700 hover:bg-gray-100">Contact</a>
    </div>
  {/if}
</nav>
