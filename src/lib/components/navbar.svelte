<script>
  let { currentPage = '' } = $props();
  let mobileMenuOpen = $state(false);
</script>

<nav class="fixed top-0 left-0 right-0 z-50 bg-background/95 backdrop-blur-sm border-b border-border">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="flex items-center justify-between h-16">
      <a href="/" class="flex items-center gap-2">
        <div class="w-8 h-8 rounded-lg bg-primary flex items-center justify-center">
          <span class="text-primary-foreground font-bold text-sm">C</span>
        </div>
        <span class="font-semibold text-lg text-foreground">ConnectED</span>
      </a>

      <!-- Desktop Navigation -->
      <div class="hidden md:flex items-center gap-8">
        <a href="/" class="text-sm font-medium transition-colors {currentPage === 'home' ? 'text-primary' : 'text-muted-foreground hover:text-foreground'}">
          Home
        </a>
        <a href="/students" class="text-sm font-medium transition-colors {currentPage === 'students' ? 'text-primary' : 'text-muted-foreground hover:text-foreground'}">
          Students / Researchers
        </a>
        <a href="/universities" class="text-sm font-medium transition-colors {currentPage === 'universities' ? 'text-primary' : 'text-muted-foreground hover:text-foreground'}">
          Universities / Partners
        </a>
        <a href="/about" class="text-sm font-medium transition-colors {currentPage === 'about' ? 'text-primary' : 'text-muted-foreground hover:text-foreground'}">
          About
        </a>
        <a href="/contact" class="text-sm font-medium transition-colors {currentPage === 'contact' ? 'text-primary' : 'text-muted-foreground hover:text-foreground'}">
          Contact
        </a>
      </div>

      <!-- Mobile Menu Button -->
      <button
        class="md:hidden p-2 rounded-lg hover:bg-secondary transition-colors"
        onclick={() => mobileMenuOpen = !mobileMenuOpen}
        aria-label="Toggle menu"
        aria-expanded={mobileMenuOpen}
      >
        {#if mobileMenuOpen}
          <svg class="w-6 h-6 text-foreground" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
          </svg>
        {:else}
          <svg class="w-6 h-6 text-foreground" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
          </svg>
        {/if}
      </button>
    </div>

    <!-- Mobile Navigation -->
    {#if mobileMenuOpen}
      <div class="md:hidden py-4 border-t border-border">
        <div class="flex flex-col gap-4">
          <a href="/" class="text-sm font-medium py-2 {currentPage === 'home' ? 'text-primary' : 'text-muted-foreground'}">
            Home
          </a>
          <a href="/students" class="text-sm font-medium py-2 {currentPage === 'students' ? 'text-primary' : 'text-muted-foreground'}">
            Students / Researchers
          </a>
          <a href="/universities" class="text-sm font-medium py-2 {currentPage === 'universities' ? 'text-primary' : 'text-muted-foreground'}">
            Universities / Partners
          </a>
          <a href="/about" class="text-sm font-medium py-2 {currentPage === 'about' ? 'text-primary' : 'text-muted-foreground'}">
            About
          </a>
          <a href="/contact" class="text-sm font-medium py-2 {currentPage === 'contact' ? 'text-primary' : 'text-muted-foreground'}">
            Contact
          </a>
        </div>
      </div>
    {/if}
  </div>
</nav>
