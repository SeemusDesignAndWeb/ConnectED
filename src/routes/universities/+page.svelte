<script>
  import Navbar from '$lib/components/navbar.svelte';
  import Footer from '$lib/components/footer.svelte';
  import FeatureCard from '$lib/components/feature-card.svelte';
  import PainPointItem from '$lib/components/pain-point-item.svelte';

  const matchingIcon = `<svg class="w-6 h-6 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" /></svg>`;
  
  const workflowIcon = `<svg class="w-6 h-6 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-3 7h3m-3 4h3m-6-4h.01M9 16h.01" /></svg>`;
  
  const adminIcon = `<svg class="w-6 h-6 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 11H5m14 0a2 2 0 012 2v6a2 2 0 01-2 2H5a2 2 0 01-2-2v-6a2 2 0 012-2m14 0V9a2 2 0 00-2-2M5 11V9a2 2 0 012-2m0 0V5a2 2 0 012-2h6a2 2 0 012 2v2M7 7h10" /></svg>`;
  
  const insightIcon = `<svg class="w-6 h-6 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z" /></svg>`;
  
  const outcomeIcon = `<svg class="w-6 h-6 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7h8m0 0v8m0-8l-8 8-4-4-6 6" /></svg>`;

  const painPoints = [
    "Heavy administrative load across the research lifecycle",
    "Poor alignment between applicant capabilities and supervisor capacity",
    "Low visibility into researcher development and progress",
    "Inefficient supervision workflows with limited standardization",
    "Increasing pressure to support diverse career outcomes",
    "Fragmented systems that don't communicate with each other"
  ];
</script>

<svelte:head>
  <title>Universities & Partners – ConnectED</title>
  <meta name="description" content="ConnectED provides efficiency and quality solutions for institutions supporting PhD researchers and doctoral programmes." />
</svelte:head>

<Navbar currentPage="universities" />

<main>
  <!-- Hero Section -->
  <section class="pt-32 pb-16 px-4 sm:px-6 lg:px-8 bg-secondary">
    <div class="max-w-4xl mx-auto text-center">
      <span class="inline-flex items-center px-3 py-1 rounded-full bg-primary/10 text-primary text-sm font-medium mb-6">
        For Universities & Partners
      </span>
      <h1 class="text-4xl sm:text-5xl font-semibold text-foreground mb-6 font-serif text-balance">
        Efficiency and quality for your institution
      </h1>
      <p class="text-lg text-muted-foreground max-w-2xl mx-auto leading-relaxed">
        ConnectED helps universities and research partners streamline doctoral programmes, improve supervision workflows, and achieve better outcomes for researchers and institutions alike.
      </p>
    </div>
  </section>

  <!-- Pain Points Section -->
  <section class="py-20 px-4 sm:px-6 lg:px-8">
    <div class="max-w-4xl mx-auto">
      <div class="text-center mb-12">
        <span class="text-primary text-sm font-medium uppercase tracking-wider">Institutional Challenges</span>
        <h2 class="text-3xl font-semibold text-foreground mt-4 font-serif">
          We understand the pressures you face
        </h2>
      </div>
      <div class="bg-card rounded-2xl border border-border p-8 lg:p-10">
        <ul class="space-y-4">
          {#each painPoints as point}
            <PainPointItem text={point} />
          {/each}
        </ul>
      </div>
    </div>
  </section>

  <!-- Benefits Section -->
  <section class="py-20 px-4 sm:px-6 lg:px-8 bg-secondary">
    <div class="max-w-7xl mx-auto">
      <div class="text-center mb-16">
        <span class="text-primary text-sm font-medium uppercase tracking-wider">Our Solutions</span>
        <h2 class="text-3xl sm:text-4xl font-semibold text-foreground mt-4 font-serif text-balance">
          How ConnectED benefits your institution
        </h2>
      </div>

      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
        <FeatureCard 
          title="Better Aligned Applicants"
          description="AI-supported matching ensures applicants are paired with the right supervisors. Improved proposal quality means better-prepared candidates from day one."
          icon={matchingIcon}
        />
        <FeatureCard 
          title="Efficient Supervisor Workflows"
          description="Standardised profiles and readiness indicators help supervisors manage their time effectively. Clear expectations reduce friction and improve outcomes."
          icon={workflowIcon}
        />
        <FeatureCard 
          title="Reduced Administrative Burden"
          description="The portable Researcher Passport eliminates repeated checks and paperwork. Verified credentials follow researchers, saving time across the institution."
          icon={adminIcon}
        />
        <FeatureCard 
          title="Insight into Researcher Development"
          description="Track skills progression and confidence indicators throughout the PhD journey. Data-driven insights help identify and support researchers who need extra guidance."
          icon={insightIcon}
        />
        <FeatureCard 
          title="Improved Institutional Outcomes"
          description="Higher completion rates and stronger alumni trajectories reflect well on your institution. ConnectED helps you achieve the outcomes that matter most."
          icon={outcomeIcon}
        />
        <div class="bg-primary rounded-xl p-8 flex flex-col justify-center">
          <h3 class="text-lg font-semibold text-primary-foreground mb-3">Ready to transform your doctoral programme?</h3>
          <p class="text-primary-foreground/80 text-sm leading-relaxed mb-6">
            Join leading universities who are improving efficiency and outcomes with ConnectED.
          </p>
          <a href="/contact" class="inline-flex items-center text-sm font-medium text-primary-foreground hover:underline">
            Explore partnership options
            <svg class="w-4 h-4 ml-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
            </svg>
          </a>
        </div>
      </div>
    </div>
  </section>

  <!-- Detailed Benefits -->
  <section class="py-20 px-4 sm:px-6 lg:px-8">
    <div class="max-w-7xl mx-auto">
      <div class="grid lg:grid-cols-2 gap-16 items-center mb-20">
        <div>
          <span class="text-primary text-sm font-medium uppercase tracking-wider">Better Matching</span>
          <h2 class="text-3xl font-semibold text-foreground mt-4 mb-6 font-serif">
            AI-powered applicant-supervisor matching
          </h2>
          <p class="text-muted-foreground leading-relaxed mb-6">
            Our intelligent matching system analyzes research interests, methodological approaches, and supervisor capacity to create optimal pairings. This leads to better-prepared applicants and more productive supervisory relationships.
          </p>
          <ul class="space-y-3">
            <li class="flex items-center gap-3">
              <svg class="w-5 h-5 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
              </svg>
              <span class="text-muted-foreground">Research interest alignment</span>
            </li>
            <li class="flex items-center gap-3">
              <svg class="w-5 h-5 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
              </svg>
              <span class="text-muted-foreground">Supervisor capacity management</span>
            </li>
            <li class="flex items-center gap-3">
              <svg class="w-5 h-5 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
              </svg>
              <span class="text-muted-foreground">Improved proposal quality</span>
            </li>
          </ul>
        </div>
        <div class="bg-secondary rounded-2xl p-8 lg:p-12">
          <img src="/placeholder.svg?height=400&width=500" alt="University campus" class="rounded-xl w-full h-auto" />
        </div>
      </div>

      <div class="grid lg:grid-cols-2 gap-16 items-center">
        <div class="order-2 lg:order-1 bg-secondary rounded-2xl p-8 lg:p-12">
          <img src="/placeholder.svg?height=400&width=500" alt="Analytics dashboard" class="rounded-xl w-full h-auto" />
        </div>
        <div class="order-1 lg:order-2">
          <span class="text-primary text-sm font-medium uppercase tracking-wider">Data-Driven Insights</span>
          <h2 class="text-3xl font-semibold text-foreground mt-4 mb-6 font-serif">
            Visibility into researcher development
          </h2>
          <p class="text-muted-foreground leading-relaxed mb-6">
            ConnectED provides comprehensive insights into researcher progress, skills development, and confidence indicators. Identify researchers who may need additional support early, and track outcomes across your doctoral programme.
          </p>
          <ul class="space-y-3">
            <li class="flex items-center gap-3">
              <svg class="w-5 h-5 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
              </svg>
              <span class="text-muted-foreground">Skills progression tracking</span>
            </li>
            <li class="flex items-center gap-3">
              <svg class="w-5 h-5 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
              </svg>
              <span class="text-muted-foreground">Early intervention indicators</span>
            </li>
            <li class="flex items-center gap-3">
              <svg class="w-5 h-5 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
              </svg>
              <span class="text-muted-foreground">Programme-wide outcome analysis</span>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>

  <!-- CTA Section -->
  <section class="py-24 px-4 sm:px-6 lg:px-8 bg-primary">
    <div class="max-w-4xl mx-auto text-center">
      <h2 class="text-3xl sm:text-4xl font-semibold text-primary-foreground mb-6 font-serif text-balance">
        Explore partnership opportunities with ConnectED
      </h2>
      <p class="text-lg text-primary-foreground/80 max-w-2xl mx-auto mb-10 leading-relaxed">
        Join leading institutions who are transforming their doctoral programmes. Let's discuss how ConnectED can support your strategic goals.
      </p>
      <a 
        href="/contact" 
        class="inline-flex items-center justify-center px-8 py-4 text-base font-medium rounded-xl bg-card text-foreground hover:bg-card/90 transition-colors"
      >
        Contact Us About Partnerships
      </a>
    </div>
  </section>
</main>

<Footer />
