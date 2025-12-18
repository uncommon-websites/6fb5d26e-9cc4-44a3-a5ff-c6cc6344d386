<script>
    const cards = [
        {
            title: "AI Communication Agents",
            image: "/generated/image-healthcare-technology-dashboard-on-compu-1766064276240-5.webp",
            color: "bg-gray-900"
        },
        {
            title: "RPA Integration",
            image: "/generated/image-healthcare-technology-dashboard-on-compu-1766064276240-5.webp",
            color: "bg-primary-600"
        },
        {
            title: "Patient Engagement",
            image: "/generated/image-patient-using-smartphone-to-book-medical-1766064269639-2.webp",
            color: "bg-primary-700"
        }
    ];
</script>

<section class="py-24 px-6 max-w-7xl mx-auto">
    <div class="flex flex-col md:flex-row justify-between items-end mb-12 gap-8">
        <div class="max-w-2xl">
            <h2 class="text-4xl md:text-5xl font-serif mb-6 leading-tight">
                The complete clinic automation platform
            </h2>
            <p class="text-gray-600 text-lg">
                HeartKraft combines AI agents and RPA to automate patient communication, appointment scheduling, insurance verification, and more. Works seamlessly with your existing EHR system.
            </p>
        </div>
        <div class="flex gap-4">
            <button class="w-12 h-12 rounded-full border border-gray-300 flex items-center justify-center hover:bg-gray-50 transition-colors">
                <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m15 18-6-6 6-6"/></svg>
            </button>
            <button class="w-12 h-12 rounded-full border border-gray-300 flex items-center justify-center hover:bg-gray-50 transition-colors">
                <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m9 18 6-6-6-6"/></svg>
            </button>
        </div>
    </div>

    <div class="grid md:grid-cols-3 gap-6">
        {#each cards as card}
            <div class="group cursor-pointer overflow-hidden rounded-lg">
                <div class="relative h-64 overflow-hidden">
                    <img src={card.image} alt={card.title} class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105" />
                </div>
                <div class="{card.color} p-6 h-32 flex items-end text-white">
                    <h3 class="text-xl font-medium">{card.title}</h3>
                </div>
            </div>
        {/each}
    </div>
</section>
