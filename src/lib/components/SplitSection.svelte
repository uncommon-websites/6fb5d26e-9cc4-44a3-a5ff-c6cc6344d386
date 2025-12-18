<script lang="ts">
    export let type: "clinicians" | "consumers" = "clinicians";
    
    const content = {
        clinicians: {
            title: "For clinic staff...",
            items: [
                { title: "Reclaim 500+ hours", desc: "Stop drowning in phone calls and admin work. Let AI handle routine patient communication automatically." },
                { title: "Reduce burnout", desc: "Free your team from repetitive tasks so they can focus on what matters: patient care." },
                { title: "Work efficiently", desc: "Automated scheduling, insurance verification, and appointment reminders that just work." }
            ],
            image: "/generated/image-happy-clinic-staff-member-smiling-while--1766064267449-1.webp",
            overlay: true
        },
        consumers: {
            title: "For patients...",
            items: [
                { title: "Get answers instantly", desc: "24/7 AI-powered responses to appointment questions, insurance queries, and clinic information." },
                { title: "Book appointments easily", desc: "Schedule, reschedule, or cancel appointments via phone, text, or web—anytime, anywhere." },
                { title: "Stay informed", desc: "Automated reminders, follow-ups, and updates keep patients engaged and reduce no-shows." }
            ],
            image: "/generated/image-patient-using-smartphone-to-book-medical-1766064269639-2.webp",
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
                         <span class="text-xs font-medium">AI handled 47 calls today</span>
                    </div>
                    <div class="space-y-2">
                        <div class="bg-gray-50 p-2 rounded">
                            <p class="text-[10px] font-semibold text-gray-500 mb-1">Appointments scheduled</p>
                            <div class="flex gap-2">
                                <div class="w-3 h-3 bg-primary-600 rounded-sm"></div>
                                <div class="h-1.5 bg-gray-200 w-20 rounded"></div>
                            </div>
                        </div>
                         <div class="bg-gray-50 p-2 rounded">
                            <p class="text-[10px] font-semibold text-gray-500 mb-1">Time saved</p>
                            <div class="h-1.5 bg-gray-200 w-full rounded mb-1"></div>
                            <div class="h-1.5 bg-gray-200 w-2/3 rounded"></div>
                        </div>
                        <div class="bg-gray-900 text-white text-[10px] p-2 rounded text-center">
                            View full automation report
                        </div>
                    </div>
                </div>
            {:else}
                 <div class="absolute bottom-10 right-4 bg-white rounded-lg shadow-lg p-4 max-w-xs w-64">
                    <div class="space-y-3">
                        <div class="bg-primary-50 p-3 rounded-lg rounded-tl-none text-xs">
                            Hi Sarah! How can I help you today?
                            <br/>
                            <div class="mt-2 text-gray-600 text-[10px]">Book appointment • Check insurance • Get directions</div>
                        </div>
                        <div class="bg-gray-100 p-3 rounded-lg rounded-tr-none ml-auto text-xs w-fit">
                            I need to schedule an appointment
                            <div class="mt-2 space-y-1">
                                <div class="flex items-center gap-2 bg-white p-1 rounded border border-gray-200">
                                    <div class="w-3 h-3 bg-primary-600 rounded-sm"></div>
                                    <span>This week</span>
                                </div>
                                <div class="flex items-center gap-2 bg-white p-1 rounded border border-gray-200">
                                    <div class="w-3 h-3 border border-gray-300 rounded-sm"></div>
                                    <span>Next week</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            {/if}
        </div>
    </div>
</div>
