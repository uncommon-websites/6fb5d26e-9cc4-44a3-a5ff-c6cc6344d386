<script>
    const news = [
        {
            tag: "Company News",
            source: "HeartKraft Blog",
            title: "HeartKraft launches AI-powered clinic automation for small practices",
            date: "January 15, 2025"
        },
        {
            tag: "Product Update",
            source: "HeartKraft Blog",
            title: "New RPA integration makes legacy EHR compatibility seamless",
            date: "January 8, 2025"
        },
        {
            tag: "Success Story",
            source: "HeartKraft Blog",
            title: "How one clinic saved 620 hours in their first year with HeartKraft",
            date: "December 20, 2024"
        }
    ];
</script>

<section class="py-24 px-6 max-w-7xl mx-auto border-t border-gray-100">
    <div class="flex justify-between items-end mb-12">
        <div>
            <h2 class="text-4xl md:text-5xl font-serif mb-8">Latest updates</h2>
            <div class="flex gap-4">
                <button class="w-12 h-12 rounded-full border border-gray-300 flex items-center justify-center hover:bg-gray-50 transition-colors">
                    <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m15 18-6-6 6-6"/></svg>
                </button>
                <button class="w-12 h-12 rounded-full border border-gray-300 flex items-center justify-center hover:bg-gray-50 transition-colors">
                    <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m9 18 6-6-6-6"/></svg>
                </button>
            </div>
        </div>
        <a href="#" class="hidden md:inline-flex items-center gap-2 font-medium hover:gap-3 transition-all mb-2">
            View all
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14"/><path d="m12 5 7 7-7 7"/></svg>
        </a>
    </div>

    <div class="grid md:grid-cols-3 gap-8">
        {#each news as item}
            <div class="group cursor-pointer">
                <div class="flex items-center gap-3 mb-4">
                    <span class="bg-primary-100 text-primary-800 text-xs font-semibold px-2 py-1 rounded">{item.tag}</span>
                    <span class="text-xs font-medium text-gray-500 uppercase tracking-wide">{item.source}</span>
                </div>
                <h3 class="text-xl font-medium mb-4 group-hover:text-primary-600 transition-colors line-clamp-3">
                    {item.title}
                </h3>
                <p class="text-xs text-gray-400 mb-8">{item.date}</p>
                <span class="text-sm font-medium inline-flex items-center gap-2 group-hover:gap-3 transition-all">
                    Read more
                    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14"/><path d="m12 5 7 7-7 7"/></svg>
                </span>
            </div>
        {/each}
    </div>
    
    <!-- Progress bar -->
    <div class="mt-12 w-full h-1 bg-gray-100 rounded-full overflow-hidden">
        <div class="w-1/3 h-full bg-gray-900 rounded-full"></div>
    </div>
</section>
