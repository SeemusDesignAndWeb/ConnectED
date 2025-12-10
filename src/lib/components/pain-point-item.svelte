<script>
  let { text } = $props();
</script>

<li class="flex items-start gap-3">
  <div class="w-5 h-5 rounded-full bg-muted flex items-center justify-center mt-0.5 shrink-0">
    <svg class="w-3 h-3 text-muted-foreground" fill="none" stroke="currentColor" viewBox="0 0 24 24">
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-3L13.732 4c-.77-1.333-2.694-1.333-3.464 0L3.34 16c-.77 1.333.192 3 1.732 3z" />
    </svg>
  </div>
  <span class="text-muted-foreground leading-relaxed">{text}</span>
</li>
