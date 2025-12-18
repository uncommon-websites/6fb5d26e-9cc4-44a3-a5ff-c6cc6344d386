<script lang="ts">
    import { fade } from 'svelte/transition';
    
    let activeTab = 0;
    const features = [
        {
            title: "Save 500+ Hours Annually",
            description: "Automate patient communication, appointment scheduling, and routine inquiries. Free your staff from drowning in calls and admin work.",
            link: "Learn more"
        },
        {
            title: "Seamless EHR Integration",
            description: "Works with any legacy system through RPA or API integration. No expensive EHR migration needed—we overcome integration fears with proven compatibility.",
            link: "Learn more"
        },
        {
            title: "AI-Powered Communication",
            description: "Intelligent AI agents handle patient calls, texts, and emails 24/7. Deliver better patient experiences while reducing staff burden.",
            link: "Learn more"
        }
    ];
</script>

<section class="bg-gray-50 py-24">
    <div class="max-w-7xl mx-auto px-6">
        <h2 class="text-4xl md:text-5xl font-serif max-w-3xl mb-16 leading-tight">
            Automate clinic communication and reclaim your team's time
        </h2>

        <div class="grid md:grid-cols-2 gap-16 items-center">
            <!-- Graphic -->
            <div class="relative flex justify-center items-center h-[400px]">
                <!-- Abstract concentric circles/radar effect -->
                <div class="absolute w-[400px] h-[400px] border border-primary-200 rounded-full opacity-30"></div>
                <div class="absolute w-[300px] h-[300px] border border-primary-300 rounded-full opacity-40"></div>
                <div class="absolute w-[200px] h-[200px] border border-primary-400 rounded-full opacity-50"></div>
                <div class="absolute w-[100px] h-[100px] border border-primary-500 rounded-full opacity-60 bg-primary-100/20 backdrop-blur-sm"></div>
                
                <!-- Floating cards -->
                <div class="absolute top-1/4 right-10 bg-white/90 backdrop-blur p-3 rounded-lg shadow-lg text-xs flex items-center gap-2 animate-pulse">
                    <div class="w-2 h-2 bg-green-500 rounded-full"></div>
                    Call answered by AI
                </div>
                <div class="absolute bottom-1/3 left-10 bg-white/90 backdrop-blur p-3 rounded-lg shadow-lg text-xs flex items-center gap-2">
                     <div class="w-2 h-2 bg-primary-600 rounded-full"></div>
                    Appointment scheduled automatically
                </div>
            </div>

            <!-- Accordion -->
            <div class="space-y-4">
                {#each features as feature, i}
                    <div class="border-b border-gray-200 pb-4">
                        <button 
                            class="w-full flex justify-between items-center py-4 text-left group"
                            on:click={() => activeTab = activeTab === i ? -1 : i}
                        >
                            <span class="text-xl font-medium {activeTab === i ? 'text-gray-900' : 'text-gray-600 group-hover:text-gray-900'}">
                                {feature.title}
                            </span>
                            <span class="text-2xl font-light text-primary-600">
                                {activeTab === i ? '−' : '+'}
                            </span>
                        </button>
                        {#if activeTab === i}
                            <div transition:fade={{ duration: 200 }} class="pb-4 pl-0 text-gray-600">
                                <p class="mb-4">{feature.description}</p>
                                <a href="#" class="text-gray-900 font-medium inline-flex items-center gap-1 hover:gap-2 transition-all">
                                    {feature.link}
                                    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14"/><path d="m12 5 7 7-7 7"/></svg>
                                </a>
                            </div>
                        {/if}
                    </div>
                {/each}
            </div>
        </div>
    </div>
</section>
