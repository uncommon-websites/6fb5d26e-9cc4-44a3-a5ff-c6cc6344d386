<script>
    const partners = [
        { name: 'SSM Health', logo: 'SSM Health' },
        { name: 'Intermountain Health', logo: 'Intermountain Health' },
        { name: 'OSF Healthcare', logo: 'OSF HEALTHCARE' },
        { name: 'MUSC Health', logo: 'MUSC Health' },
    ];
</script>

<section class="py-12 border-t border-gray-100">
    <div class="max-w-7xl mx-auto px-6">
        <div class="flex flex-col md:flex-row justify-between items-center mb-12 gap-6">
            <h2 class="text-3xl font-serif">Partners</h2>
            <div class="flex gap-3">
                <button class="px-4 py-2 rounded-full border border-gray-300 text-sm font-medium hover:bg-gray-50 transition-colors">Health Systems</button>
                <button class="px-4 py-2 rounded-full border border-gray-300 text-sm font-medium hover:bg-gray-50 transition-colors">Health Plans</button>
                <button class="px-4 py-2 rounded-full border border-gray-300 text-sm font-medium hover:bg-gray-50 transition-colors">Employers</button>
            </div>
        </div>

        <div class="grid grid-cols-2 md:grid-cols-4 gap-12 items-center">
            <!-- Simple SVG placeholders for logos -->
            <div class="flex justify-center opacity-50 grayscale hover:grayscale-0 hover:opacity-100 transition-all duration-500 cursor-pointer">
                 <!-- SSM Healthish logo -->
                 <svg height="40" viewBox="0 0 200 60" fill="currentColor" class="h-8 md:h-10">
                    <path d="M20,30 Q30,10 50,30 T80,30" stroke="currentColor" stroke-width="5" fill="none"/>
                    <text x="90" y="38" font-family="sans-serif" font-weight="bold" font-size="24">SSMHealth.</text>
                 </svg>
            </div>
            <div class="flex justify-center opacity-50 grayscale hover:grayscale-0 hover:opacity-100 transition-all duration-500 cursor-pointer">
                <!-- Intermountain -->
                 <div class="flex items-center gap-2">
                    <div class="font-bold text-3xl">i</div>
                    <div class="flex flex-col leading-none">
                        <span class="font-bold text-sm">Intermountain</span>
                        <span class="font-light text-sm">Health</span>
                    </div>
                 </div>
            </div>
            <div class="flex justify-center opacity-50 grayscale hover:grayscale-0 hover:opacity-100 transition-all duration-500 cursor-pointer">
                <!-- OSF -->
                <div class="flex items-center gap-2">
                    <div class="border-2 border-current rounded-full p-1 w-8 h-8 flex items-center justify-center font-serif font-bold text-xs">OSF</div>
                    <div class="flex flex-col leading-none">
                        <span class="font-bold text-sm">OSF</span>
                        <span class="text-[10px] tracking-widest uppercase">Healthcare</span>
                    </div>
                 </div>
            </div>
            <div class="flex justify-center opacity-50 grayscale hover:grayscale-0 hover:opacity-100 transition-all duration-500 cursor-pointer">
                 <!-- MUSC -->
                 <div class="flex items-center gap-2">
                    <div class="w-8 h-8 bg-current rounded-full opacity-20"></div>
                    <div class="flex flex-col leading-none">
                        <span class="font-serif font-bold text-sm">MUSC Health</span>
                        <span class="text-[8px] text-gray-500">Medical University of South Carolina</span>
                    </div>
                 </div>
            </div>
        </div>
    </div>
</section>
