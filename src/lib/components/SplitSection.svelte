<script lang="ts">
    export let type: "clinicians" | "consumers" = "clinicians";
    
    const content = {
        clinicians: {
            title: "For clinicians...",
            items: [
                { title: "Move Faster", desc: "With automated symptom collection, documentation, prescriptions, and lab orders." },
                { title: "Work smarter", desc: "Thanks to readily available, evidence-based decision support." },
                { title: "Care better", desc: "Optimize resource allocation and patient flow." }
            ],
            image: "https://images.unsplash.com/photo-1559839734-2b71ea197ec2?w=800&q=80",
            overlay: true
        },
        consumers: {
            title: "For consumers...",
            items: [
                { title: "Start anywhere", desc: "Gain digital-first access to care wherever and whenever." },
                { title: "Know more", desc: "With simple step-by-step guides across the journey." },
                { title: "Stay connected", desc: "Through sleek experiences that keep them happy and coming back." }
            ],
            image: "https://images.unsplash.com/photo-1522071820081-009f0129c71c?w=800&q=80",
            overlay: false
        }
    };

    $: data = content[type];
</script>

<div class="grid md:grid-cols-2 gap-16 items-center">
    <div class="{type === 'consumers' ? 'md:order-2' : ''}">
        <h3 class="text-2xl font-serif mb-8">{data.title}</h3>
        <ul class="space-y-8 mb-10">
            {#each data.items as item}
                <li class="flex gap-4">
                    <div class="mt-1 text-gray-400">
                        <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="20 6 9 17 4 12"/></svg>
                    </div>
                    <div>
                        <h4 class="font-medium text-lg mb-1">{item.title}</h4>
                        <p class="text-gray-600 text-sm leading-relaxed">{item.desc}</p>
                    </div>
                </li>
            {/each}
        </ul>
        <button class="border border-gray-300 px-6 py-2.5 rounded-full text-sm font-medium hover:bg-gray-50 transition-colors">
            Request a demo
        </button>
    </div>

    <div class="relative {type === 'consumers' ? 'md:order-1' : ''}">
        <div class="relative rounded-lg overflow-hidden shadow-xl">
            <img src={data.image} alt={type} class="w-full h-[500px] object-cover" />
            
            <!-- Overlay UI Mockups -->
            {#if type === 'clinicians'}
                <div class="absolute top-1/2 left-4 right-4 transform -translate-y-1/2 bg-white rounded-lg shadow-lg p-4 max-w-xs">
                    <div class="flex items-center gap-2 mb-3 border-b border-gray-100 pb-2">
                         <div class="w-2 h-2 bg-green-500 rounded-full"></div>
                         <span class="text-xs font-medium">Melanie (34) attests to experiencing abdominal pain</span>
                    </div>
                    <div class="space-y-2">
                        <div class="bg-gray-50 p-2 rounded">
                            <p class="text-[10px] font-semibold text-gray-500 mb-1">Recommended diagnoses</p>
                            <div class="flex gap-2">
                                <div class="w-3 h-3 bg-fabric-dark rounded-sm"></div>
                                <div class="h-1.5 bg-gray-200 w-20 rounded"></div>
                            </div>
                        </div>
                         <div class="bg-gray-50 p-2 rounded">
                            <p class="text-[10px] font-semibold text-gray-500 mb-1">Discharge patient</p>
                            <div class="h-1.5 bg-gray-200 w-full rounded mb-1"></div>
                            <div class="h-1.5 bg-gray-200 w-2/3 rounded"></div>
                        </div>
                        <div class="bg-fabric-dark text-white text-[10px] p-2 rounded text-center">
                            Send care plan and begin discharge
                        </div>
                    </div>
                </div>
            {:else}
                 <div class="absolute bottom-10 right-4 bg-white rounded-lg shadow-lg p-4 max-w-xs w-64">
                    <div class="space-y-3">
                        <div class="bg-pink-50 p-3 rounded-lg rounded-tl-none text-xs">
                            Welcome, Melanie
                            <br/>
                            Please start your intake
                             <div class="mt-2 bg-fabric-dark text-white inline-block px-2 py-1 rounded-full text-[10px]">Get started</div>
                        </div>
                        <div class="bg-gray-100 p-3 rounded-lg rounded-tr-none ml-auto text-xs w-fit">
                            Was the onset of abdominal pain sudden?
                            <div class="mt-2 space-y-1">
                                <div class="flex items-center gap-2 bg-white p-1 rounded border border-gray-200">
                                    <div class="w-3 h-3 bg-fabric-dark rounded-sm"></div>
                                    <span>Yes</span>
                                </div>
                                <div class="flex items-center gap-2 bg-white p-1 rounded border border-gray-200">
                                    <div class="w-3 h-3 border border-gray-300 rounded-sm"></div>
                                    <span>No</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            {/if}
        </div>
    </div>
</div>
