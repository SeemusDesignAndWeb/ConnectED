<script>
  let { title, description, icon } = $props();
</script>

<div class="bg-card rounded-xl p-8 border border-border hover:border-primary/30 hover:shadow-lg transition-all duration-300">
  <div class="w-12 h-12 rounded-lg bg-primary/10 flex items-center justify-center mb-6">
    {@html icon}
  </div>
  <h3 class="text-lg font-semibold text-card-foreground mb-3">{title}</h3>
  <p class="text-muted-foreground text-sm leading-relaxed">{description}</p>
</div>
