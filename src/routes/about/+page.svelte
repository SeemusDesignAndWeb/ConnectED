<script>
  import Navbar from '$lib/components/navbar.svelte';
  import Footer from '$lib/components/footer.svelte';
</script>

<svelte:head>
  <title>About – ConnectED</title>
  <meta name="description" content="Learn about ConnectED's mission to transform the PhD lifecycle through clarity, structure, and connection." />
</svelte:head>

<Navbar currentPage="about" />

<main>
  <!-- Hero Section -->
  <section class="pt-32 pb-16 px-4 sm:px-6 lg:px-8 bg-secondary">
    <div class="max-w-4xl mx-auto text-center">
      <h1 class="text-4xl sm:text-5xl font-semibold text-foreground mb-6 font-serif text-balance">
        About ConnectED
      </h1>
      <p class="text-lg text-muted-foreground max-w-2xl mx-auto leading-relaxed">
        We believe the PhD journey shouldn't feel isolating, unclear, or overwhelming. ConnectED exists to bring structure, support, and connection to researchers and institutions alike.
      </p>
    </div>
  </section>

  <!-- Mission Section -->
  <section class="py-20 px-4 sm:px-6 lg:px-8">
    <div class="max-w-4xl mx-auto">
      <div class="grid md:grid-cols-2 gap-12">
        <div>
          <span class="text-primary text-sm font-medium uppercase tracking-wider">Our Mission</span>
          <h2 class="text-3xl font-semibold text-foreground mt-4 mb-6 font-serif">
            Transforming the research journey
          </h2>
          <p class="text-muted-foreground leading-relaxed mb-4">
            ConnectED was founded on the understanding that the PhD lifecycle is complex, often fragmented, and rarely supported by cohesive infrastructure.
          </p>
          <p class="text-muted-foreground leading-relaxed">
            Our mission is to bring clarity to researchers, efficiency to institutions, and connection across the entire ecosystem. We believe that when students, supervisors, universities, and employers work together, everyone benefits.
          </p>
        </div>
        <div>
          <span class="text-primary text-sm font-medium uppercase tracking-wider">Our Vision</span>
          <h2 class="text-3xl font-semibold text-foreground mt-4 mb-6 font-serif">
            A connected future
          </h2>
          <p class="text-muted-foreground leading-relaxed mb-4">
            We envision a future where every researcher has a clear pathway from application to career, where institutions can support their doctoral programmes efficiently, and where the value of research is visible to society.
          </p>
          <p class="text-muted-foreground leading-relaxed">
            ConnectED is building the infrastructure to make this vision a reality, one connection at a time.
          </p>
        </div>
      </div>
    </div>
  </section>

  <!-- Values Section -->
  <section class="py-20 px-4 sm:px-6 lg:px-8 bg-secondary">
    <div class="max-w-7xl mx-auto">
      <div class="text-center mb-16">
        <span class="text-primary text-sm font-medium uppercase tracking-wider">Our Values</span>
        <h2 class="text-3xl font-semibold text-foreground mt-4 font-serif">
          What guides us
        </h2>
      </div>

      <div class="grid md:grid-cols-3 gap-8">
        <div class="bg-card rounded-xl p-8 border border-border">
          <div class="w-12 h-12 rounded-lg bg-primary/10 flex items-center justify-center mb-6">
            <svg class="w-6 h-6 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197M13 7a4 4 0 11-8 0 4 4 0 018 0z" />
            </svg>
          </div>
          <h3 class="text-lg font-semibold text-card-foreground mb-3">Human-Centred</h3>
          <p class="text-muted-foreground text-sm leading-relaxed">
            We design for real people with real challenges. Every feature starts with understanding the human experience.
          </p>
        </div>
        <div class="bg-card rounded-xl p-8 border border-border">
          <div class="w-12 h-12 rounded-lg bg-primary/10 flex items-center justify-center mb-6">
            <svg class="w-6 h-6 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
            </svg>
          </div>
          <h3 class="text-lg font-semibold text-card-foreground mb-3">Clarity</h3>
          <p class="text-muted-foreground text-sm leading-relaxed">
            We bring structure to complexity without oversimplifying. Clear pathways, clear expectations, clear outcomes.
          </p>
        </div>
        <div class="bg-card rounded-xl p-8 border border-border">
          <div class="w-12 h-12 rounded-lg bg-primary/10 flex items-center justify-center mb-6">
            <svg class="w-6 h-6 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13.828 10.172a4 4 0 00-5.656 0l-4 4a4 4 0 105.656 5.656l1.102-1.101m-.758-4.899a4 4 0 005.656 0l4-4a4 4 0 00-5.656-5.656l-1.1 1.1" />
            </svg>
          </div>
          <h3 class="text-lg font-semibold text-card-foreground mb-3">Connection</h3>
          <p class="text-muted-foreground text-sm leading-relaxed">
            We build bridges between students, supervisors, institutions, and employers. Together, we achieve more.
          </p>
        </div>
      </div>
    </div>
  </section>

  <!-- Closing CTA -->
  <section class="py-20 px-4 sm:px-6 lg:px-8">
    <div class="max-w-4xl mx-auto text-center">
      <h2 class="text-3xl font-semibold text-foreground mb-6 font-serif">
        Join the ConnectED community
      </h2>
      <p class="text-muted-foreground max-w-2xl mx-auto mb-10 leading-relaxed">
        Whether you're a researcher starting your journey or an institution looking to improve outcomes, we're here to help.
      </p>
      <div class="flex flex-col sm:flex-row gap-4 justify-center">
        <a 
          href="/students" 
          class="inline-flex items-center justify-center px-6 py-3 text-sm font-medium rounded-xl bg-primary text-primary-foreground hover:bg-primary/90 transition-colors"
        >
          For Students / Researchers
        </a>
        <a 
          href="/universities" 
          class="inline-flex items-center justify-center px-6 py-3 text-sm font-medium rounded-xl bg-card text-card-foreground border border-border hover:bg-secondary transition-colors"
        >
          For Universities / Partners
        </a>
      </div>
    </div>
  </section>
</main>

<Footer />
