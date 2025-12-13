<script lang="ts">
  import { onMount } from 'svelte';

  let isScrolled = false;

  onMount(() => {
    const handleScroll = () => {
      isScrolled = window.scrollY > 10;
    };
    window.addEventListener('scroll', handleScroll);
    return () => window.removeEventListener('scroll', handleScroll);
  });
</script>

<header class="fixed top-0 left-0 right-0 z-50 transition-all duration-300 {isScrolled ? 'bg-white/90 backdrop-blur-md shadow-sm py-3' : 'bg-transparent py-5'}">
  <div class="max-w-7xl mx-auto px-6 flex items-center justify-between">
    <!-- Logo -->
    <a href="/" class="flex items-center gap-2">
      <span class="font-serif text-3xl font-bold tracking-tight">fabric</span>
    </a>

    <!-- Navigation -->
    <nav class="hidden md:flex items-center gap-8">
      <a href="#platform" class="text-sm font-medium hover:text-gray-600">Platform & Services</a>
      <a href="#solutions" class="text-sm font-medium hover:text-gray-600">Solutions</a>
      <a href="#resources" class="text-sm font-medium hover:text-gray-600">Resources</a>
    </nav>

    <!-- Actions -->
    <div class="flex items-center gap-4">
      <button class="p-2 hover:bg-gray-100 rounded-full" aria-label="Search">
        <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-search"><circle cx="11" cy="11" r="8"/><path d="m21 21-4.3-4.3"/></svg>
      </button>
      <a href="#demo" class="bg-fabric-blue hover:bg-fabric-blue-dark text-fabric-dark px-5 py-2.5 rounded-full text-sm font-medium transition-colors">
        Request a demo
      </a>
    </div>
  </div>
</header>
