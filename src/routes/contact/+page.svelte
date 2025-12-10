<script>
  import Navbar from '$lib/components/navbar.svelte';
  import Footer from '$lib/components/footer.svelte';

  let formData = $state({
    name: '',
    email: '',
    organization: '',
    type: '',
    message: ''
  });

  let submitted = $state(false);

  function handleSubmit(event) {
    event.preventDefault();
    // In a real app, this would send the form data to an API
    console.log('[v0] Form submitted:', formData);
    submitted = true;
  }
</script>

<svelte:head>
  <title>Contact – ConnectED</title>
  <meta name="description" content="Get in touch with ConnectED. We're here to help students, researchers, and institutions." />
</svelte:head>

<Navbar currentPage="contact" />

<main>
  <!-- Hero Section -->
  <section class="pt-32 pb-16 px-4 sm:px-6 lg:px-8 bg-secondary">
    <div class="max-w-4xl mx-auto text-center">
      <h1 class="text-4xl sm:text-5xl font-semibold text-foreground mb-6 font-serif text-balance">
        Get in Touch
      </h1>
      <p class="text-lg text-muted-foreground max-w-2xl mx-auto leading-relaxed">
        Whether you're a student seeking clarity, a researcher looking for support, or an institution exploring partnership, we'd love to hear from you.
      </p>
    </div>
  </section>

  <!-- Contact Form Section -->
  <section class="py-20 px-4 sm:px-6 lg:px-8">
    <div class="max-w-4xl mx-auto">
      <div class="grid lg:grid-cols-5 gap-12">
        <!-- Contact Info -->
        <div class="lg:col-span-2">
          <h2 class="text-2xl font-semibold text-foreground mb-6 font-serif">
            Let's connect
          </h2>
          <p class="text-muted-foreground leading-relaxed mb-8">
            Fill out the form and our team will get back to you within 48 hours. You can also reach us directly through the channels below.
          </p>

          <div class="space-y-6">
            <div class="flex items-start gap-4">
              <div class="w-10 h-10 rounded-lg bg-primary/10 flex items-center justify-center shrink-0">
                <svg class="w-5 h-5 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                </svg>
              </div>
              <div>
                <h4 class="font-medium text-foreground mb-1">Email</h4>
                <a href="mailto:hello@connected.edu" class="text-sm text-primary hover:underline">hello@connected.edu</a>
              </div>
            </div>
            <div class="flex items-start gap-4">
              <div class="w-10 h-10 rounded-lg bg-primary/10 flex items-center justify-center shrink-0">
                <svg class="w-5 h-5 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
                </svg>
              </div>
              <div>
                <h4 class="font-medium text-foreground mb-1">Office</h4>
                <p class="text-sm text-muted-foreground">Innovation Hub, Research Park<br />Cambridge, UK</p>
              </div>
            </div>
            <div class="flex items-start gap-4">
              <div class="w-10 h-10 rounded-lg bg-primary/10 flex items-center justify-center shrink-0">
                <svg class="w-5 h-5 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
                </svg>
              </div>
              <div>
                <h4 class="font-medium text-foreground mb-1">Response Time</h4>
                <p class="text-sm text-muted-foreground">Within 48 hours</p>
              </div>
            </div>
          </div>
        </div>

        <!-- Form -->
        <div class="lg:col-span-3">
          {#if submitted}
            <div class="bg-primary/10 rounded-2xl p-8 text-center">
              <div class="w-16 h-16 rounded-full bg-primary/20 flex items-center justify-center mx-auto mb-6">
                <svg class="w-8 h-8 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                </svg>
              </div>
              <h3 class="text-xl font-semibold text-foreground mb-3">Thank you for reaching out!</h3>
              <p class="text-muted-foreground">We've received your message and will get back to you within 48 hours.</p>
            </div>
          {:else}
            <form onsubmit={handleSubmit} class="bg-card rounded-2xl border border-border p-8">
              <div class="grid sm:grid-cols-2 gap-6 mb-6">
                <div>
                  <label for="name" class="block text-sm font-medium text-foreground mb-2">Name</label>
                  <input
                    type="text"
                    id="name"
                    bind:value={formData.name}
                    required
                    class="w-full px-4 py-3 rounded-xl border border-input bg-background text-foreground placeholder:text-muted-foreground focus:outline-none focus:ring-2 focus:ring-ring"
                    placeholder="Your name"
                  />
                </div>
                <div>
                  <label for="email" class="block text-sm font-medium text-foreground mb-2">Email</label>
                  <input
                    type="email"
                    id="email"
                    bind:value={formData.email}
                    required
                    class="w-full px-4 py-3 rounded-xl border border-input bg-background text-foreground placeholder:text-muted-foreground focus:outline-none focus:ring-2 focus:ring-ring"
                    placeholder="you@example.com"
                  />
                </div>
              </div>

              <div class="grid sm:grid-cols-2 gap-6 mb-6">
                <div>
                  <label for="organization" class="block text-sm font-medium text-foreground mb-2">Organization (optional)</label>
                  <input
                    type="text"
                    id="organization"
                    bind:value={formData.organization}
                    class="w-full px-4 py-3 rounded-xl border border-input bg-background text-foreground placeholder:text-muted-foreground focus:outline-none focus:ring-2 focus:ring-ring"
                    placeholder="University or company"
                  />
                </div>
                <div>
                  <label for="type" class="block text-sm font-medium text-foreground mb-2">I am a...</label>
                  <select
                    id="type"
                    bind:value={formData.type}
                    required
                    class="w-full px-4 py-3 rounded-xl border border-input bg-background text-foreground focus:outline-none focus:ring-2 focus:ring-ring"
                  >
                    <option value="">Select an option</option>
                    <option value="student">Student / Researcher</option>
                    <option value="university">University / Institution</option>
                    <option value="employer">Employer / Partner</option>
                    <option value="other">Other</option>
                  </select>
                </div>
              </div>

              <div class="mb-6">
                <label for="message" class="block text-sm font-medium text-foreground mb-2">Message</label>
                <textarea
                  id="message"
                  bind:value={formData.message}
                  required
                  rows="5"
                  class="w-full px-4 py-3 rounded-xl border border-input bg-background text-foreground placeholder:text-muted-foreground focus:outline-none focus:ring-2 focus:ring-ring resize-none"
                  placeholder="How can we help you?"
                ></textarea>
              </div>

              <button
                type="submit"
                class="w-full sm:w-auto px-8 py-3 rounded-xl bg-primary text-primary-foreground font-medium hover:bg-primary/90 transition-colors"
              >
                Send Message
              </button>
            </form>
          {/if}
        </div>
      </div>
    </div>
  </section>

  <!-- FAQ Section -->
  <section class="py-20 px-4 sm:px-6 lg:px-8 bg-secondary">
    <div class="max-w-4xl mx-auto">
      <div class="text-center mb-12">
        <h2 class="text-3xl font-semibold text-foreground font-serif">
          Frequently Asked Questions
        </h2>
      </div>

      <div class="space-y-4">
        <div class="bg-card rounded-xl border border-border p-6">
          <h4 class="font-medium text-foreground mb-2">Is ConnectED free for students?</h4>
          <p class="text-sm text-muted-foreground leading-relaxed">
            ConnectED offers free core features for students and researchers. Some advanced features may be available through institutional partnerships.
          </p>
        </div>
        <div class="bg-card rounded-xl border border-border p-6">
          <h4 class="font-medium text-foreground mb-2">How do university partnerships work?</h4>
          <p class="text-sm text-muted-foreground leading-relaxed">
            We work with institutions to integrate ConnectED into existing doctoral programmes. Contact us to discuss partnership models tailored to your needs.
          </p>
        </div>
        <div class="bg-card rounded-xl border border-border p-6">
          <h4 class="font-medium text-foreground mb-2">Is my data secure?</h4>
          <p class="text-sm text-muted-foreground leading-relaxed">
            Absolutely. We take data security seriously and comply with GDPR and institutional data protection requirements. Your Researcher Passport remains under your control.
          </p>
        </div>
      </div>
    </div>
  </section>
</main>

<Footer />
