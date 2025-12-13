<script lang="ts">
    import { fade } from 'svelte/transition';
    
    let activeTab = 0;
    const features = [
        {
            title: "Intelligent Access and Answers",
            description: "Offer consumer-grade care experiences and provide the right answers and care options.",
            link: "Learn more"
        },
        {
            title: "Streamlined Care Experiences",
            description: "Automate intake and triage to reduce administrative burden and improve patient flow.",
            link: "Learn more"
        },
        {
            title: "Operational & Clinical Efficiency",
            description: "Optimize resource allocation and improve clinical decision making with data-driven insights.",
            link: "Learn more"
        }
    ];
</script>

<section class="bg-fabric-blue py-24">
    <div class="max-w-7xl mx-auto px-6">
        <h2 class="text-4xl md:text-5xl font-serif max-w-3xl mb-16 leading-tight">
            We drive better outcomes and savings for health systems, health plans, and employers
        </h2>

        <div class="grid md:grid-cols-2 gap-16 items-center">
            <!-- Graphic -->
            <div class="relative flex justify-center items-center h-[400px]">
                <!-- Abstract concentric circles/radar effect -->
                <div class="absolute w-[400px] h-[400px] border border-blue-200 rounded-full opacity-30"></div>
                <div class="absolute w-[300px] h-[300px] border border-blue-300 rounded-full opacity-40"></div>
                <div class="absolute w-[200px] h-[200px] border border-blue-400 rounded-full opacity-50"></div>
                <div class="absolute w-[100px] h-[100px] border border-blue-500 rounded-full opacity-60 bg-blue-100/20 backdrop-blur-sm"></div>
                
                <!-- Floating cards -->
                <div class="absolute top-1/4 right-10 bg-white/90 backdrop-blur p-3 rounded-lg shadow-lg text-xs flex items-center gap-2 animate-pulse">
                    <div class="w-2 h-2 bg-green-500 rounded-full"></div>
                    Patient seen virtually
                </div>
                <div class="absolute bottom-1/3 left-10 bg-white/90 backdrop-blur p-3 rounded-lg shadow-lg text-xs flex items-center gap-2">
                     <div class="w-2 h-2 bg-blue-500 rounded-full"></div>
                    Patient referred for in-person care
                </div>
            </div>

            <!-- Accordion -->
            <div class="space-y-4">
                {#each features as feature, i}
                    <div class="border-b border-blue-200 pb-4">
                        <button 
                            class="w-full flex justify-between items-center py-4 text-left group"
                            on:click={() => activeTab = activeTab === i ? -1 : i}
                        >
                            <span class="text-xl font-medium {activeTab === i ? 'text-fabric-dark' : 'text-gray-600 group-hover:text-fabric-dark'}">
                                {feature.title}
                            </span>
                            <span class="text-2xl font-light text-blue-500">
                                {activeTab === i ? '−' : '+'}
                            </span>
                        </button>
                        {#if activeTab === i}
                            <div transition:fade={{ duration: 200 }} class="pb-4 pl-0 text-gray-600">
                                <p class="mb-4">{feature.description}</p>
                                <a href="#" class="text-fabric-dark font-medium inline-flex items-center gap-1 hover:gap-2 transition-all">
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
