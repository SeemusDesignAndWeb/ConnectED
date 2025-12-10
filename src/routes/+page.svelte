<script>
  import Navbar from '$lib/components/navbar.svelte';
  import Footer from '$lib/components/footer.svelte';
</script>

<svelte:head>
  <title>ConnectED – The PhD Journey, Connected</title>
  <meta name="description" content="ConnectED brings clarity, structure, and opportunity to the PhD lifecycle. Connecting students, researchers, supervisors, and institutions." />
</svelte:head>

<Navbar currentPage="home" />

<main>
  <!-- Hero Section -->
  <section class="pt-32 pb-24 px-4 sm:px-6 lg:px-8">
    <div class="max-w-4xl mx-auto text-center">
      <h1 class="text-4xl sm:text-5xl lg:text-6xl font-semibold text-foreground mb-6 text-balance font-serif">
        ConnectED – The PhD Journey, Connected
      </h1>
      <p class="text-lg sm:text-xl text-muted-foreground max-w-2xl mx-auto mb-12 leading-relaxed text-pretty">
        ConnectED brings clarity, structure, and opportunity to the PhD lifecycle. Whether you're starting your research journey or supporting those who are, we're here to help.
      </p>
      
      <!-- Audience Pathway Buttons -->
      <div class="flex flex-col sm:flex-row gap-4 justify-center">
        <a 
          href="/students" 
          class="inline-flex items-center justify-center px-8 py-4 text-base font-medium rounded-xl bg-primary text-primary-foreground hover:bg-primary/90 transition-colors shadow-lg shadow-primary/20"
        >
          <svg class="w-5 h-5 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.747 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253" />
          </svg>
          I am a Student / Researcher
        </a>
        <a 
          href="/universities" 
          class="inline-flex items-center justify-center px-8 py-4 text-base font-medium rounded-xl bg-card text-card-foreground border border-border hover:bg-secondary transition-colors"
        >
          <svg class="w-5 h-5 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5M9 7h1m-1 4h1m4-4h1m-1 4h1m-5 10v-5a1 1 0 011-1h2a1 1 0 011 1v5m-4 0h4" />
          </svg>
          I am a University / Partner
        </a>
      </div>
    </div>
  </section>

  <!-- Visual Divider -->
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="border-t border-border"></div>
  </div>

  <!-- Overview Section -->
  <section class="py-24 px-4 sm:px-6 lg:px-8">
    <div class="max-w-7xl mx-auto">
      <div class="grid md:grid-cols-2 gap-16 items-center">
        <div>
          <span class="text-primary text-sm font-medium uppercase tracking-wider">Our Mission</span>
          <h2 class="text-3xl sm:text-4xl font-semibold text-foreground mt-4 mb-6 font-serif text-balance">
            One connected ecosystem for the entire research journey
          </h2>
          <p class="text-muted-foreground leading-relaxed mb-6">
            ConnectED brings students, researchers, supervisors, and institutions into one connected ecosystem. Students gain clarity. Universities gain efficiency. Supervisors gain insight. Employers gain visibility.
          </p>
          <p class="text-muted-foreground leading-relaxed">
            We understand that the PhD journey can feel overwhelming, fragmented, and uncertain. That's why we've built a platform that provides structure without rigidity, support without dependency, and clarity without oversimplification.
          </p>
        </div>
        <div class="bg-secondary rounded-2xl p-8 lg:p-12">
          <div class="grid grid-cols-2 gap-6">
            <div class="text-center p-6 bg-card rounded-xl">
              <div class="text-3xl font-bold text-primary mb-2">10K+</div>
              <div class="text-sm text-muted-foreground">Researchers</div>
            </div>
            <div class="text-center p-6 bg-card rounded-xl">
              <div class="text-3xl font-bold text-primary mb-2">150+</div>
              <div class="text-sm text-muted-foreground">Institutions</div>
            </div>
            <div class="text-center p-6 bg-card rounded-xl">
              <div class="text-3xl font-bold text-primary mb-2">500+</div>
              <div class="text-sm text-muted-foreground">Supervisors</div>
            </div>
            <div class="text-center p-6 bg-card rounded-xl">
              <div class="text-3xl font-bold text-primary mb-2">95%</div>
              <div class="text-sm text-muted-foreground">Satisfaction</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Shared Closing Section -->
  <section class="py-24 px-4 sm:px-6 lg:px-8 bg-secondary">
    <div class="max-w-4xl mx-auto text-center">
      <h2 class="text-3xl sm:text-4xl font-semibold text-foreground mb-6 font-serif text-balance">
        Ready to transform your research journey?
      </h2>
      <p class="text-lg text-muted-foreground max-w-2xl mx-auto mb-10 leading-relaxed">
        ConnectED brings students, researchers, supervisors, and institutions into one connected ecosystem. Students gain clarity. Universities gain efficiency. Supervisors gain insight. Employers gain visibility.
      </p>
      <div class="flex flex-col sm:flex-row gap-4 justify-center">
        <a 
          href="/students" 
          class="inline-flex items-center justify-center px-6 py-3 text-sm font-medium rounded-xl bg-primary text-primary-foreground hover:bg-primary/90 transition-colors"
        >
          Student / Researcher Path
        </a>
        <a 
          href="/universities" 
          class="inline-flex items-center justify-center px-6 py-3 text-sm font-medium rounded-xl bg-card text-card-foreground border border-border hover:bg-background transition-colors"
        >
          University / Partner Path
        </a>
      </div>
    </div>
  </section>
</main>

<Footer />
