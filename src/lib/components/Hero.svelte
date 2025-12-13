<script lang="ts">
</script>

<section class="pt-32 pb-16 md:pt-40 md:pb-24 px-6 max-w-7xl mx-auto grid md:grid-cols-2 gap-12 items-center">
  <div class="space-y-8">
    <h1 class="text-5xl md:text-7xl font-serif font-medium leading-[1.1]">
      Intelligently <br/> connected care
    </h1>
    <p class="text-lg md:text-xl text-gray-600 max-w-lg leading-relaxed">
      We simplify, automate, and unify care experiences—delivering seamless interactions, reducing care costs, and powering faster, higher-quality care at the moment of need.
    </p>
    <div class="flex flex-wrap gap-4">
      <button class="bg-fabric-dark text-white px-6 py-3 rounded-full font-medium hover:bg-gray-800 transition-colors flex items-center gap-2">
        Meet Provider Directory
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14"/><path d="m12 5 7 7-7 7"/></svg>
      </button>
      <button class="border border-gray-300 px-6 py-3 rounded-full font-medium hover:border-gray-400 transition-colors flex items-center gap-2">
        Fabric acquires <span class="font-bold">GYANT</span>
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14"/><path d="m12 5 7 7-7 7"/></svg>
      </button>
    </div>
  </div>

  <div class="relative">
    <!-- Background shape -->
    <div class="absolute -top-10 -right-10 w-[120%] h-[120%] bg-fabric-pink rounded-[3rem] -z-10 transform rotate-2"></div>
    
    <!-- UI Mockup -->
    <div class="relative bg-white rounded-xl shadow-xl p-6 md:p-8 border border-gray-100">
      <div class="flex items-center justify-between mb-6">
        <div>
          <h3 class="text-2xl font-serif">Your patient's visit summary</h3>
          <div class="flex items-center gap-2 mt-2">
            <div class="w-6 h-6 rounded-full bg-orange-800 overflow-hidden">
                <img src="https://images.unsplash.com/photo-1438761681033-6461ffad8d80?w=100&h=100&fit=crop" alt="User" class="w-full h-full object-cover" />
            </div>
            <span class="text-sm text-gray-500">Judy JAZZ</span>
          </div>
        </div>
        <div class="text-right">
            <!-- Logo placeholder -->
            <div class="flex items-center gap-1 text-blue-800 font-serif font-bold">
                <span class="text-xl">MUSC Health</span>
            </div>
        </div>
      </div>

      <div class="grid grid-cols-3 gap-4">
        <div class="col-span-1 space-y-4">
            <div class="bg-gray-50 p-3 rounded-lg border border-gray-100">
                <p class="text-xs text-gray-500 mb-2">What type of visit would you like?</p>
                <div class="grid grid-cols-2 gap-2">
                    <div class="bg-white p-2 rounded border border-gray-200 text-center">
                        <div class="w-4 h-4 mx-auto mb-1 bg-gray-200 rounded-full"></div>
                        <span class="text-[10px] block">Virtual visit</span>
                    </div>
                    <div class="bg-white p-2 rounded border border-gray-200 text-center">
                        <div class="w-4 h-4 mx-auto mb-1 bg-gray-200 rounded-full"></div>
                        <span class="text-[10px] block">In-Person visit</span>
                    </div>
                </div>
            </div>
             <div class="bg-gray-50 p-3 rounded-lg border border-gray-100">
                <p class="text-xs text-gray-500 mb-2">Do you currently have a sore throat?</p>
                <div class="space-y-1">
                    <div class="bg-white p-1.5 rounded border border-gray-200 text-[10px]">Yes</div>
                    <div class="bg-white p-1.5 rounded border border-gray-200 text-[10px]">No</div>
                </div>
            </div>
        </div>
        
        <div class="col-span-2 bg-gray-50 p-4 rounded-lg border border-gray-100">
            <div class="flex justify-between items-center mb-3">
                <span class="text-xs font-semibold">Assessment and Treatment Plan</span>
            </div>
            <div class="space-y-2">
                <div class="h-2 bg-gray-200 rounded w-3/4"></div>
                <div class="h-2 bg-gray-200 rounded w-1/2"></div>
                
                <div class="mt-4 space-y-2">
                    <div class="flex items-center gap-2">
                        <div class="w-3 h-3 bg-gray-300 rounded-sm"></div>
                        <div class="h-1.5 bg-gray-200 rounded w-full"></div>
                    </div>
                    <div class="flex items-center gap-2">
                        <div class="w-3 h-3 bg-gray-800 rounded-sm"></div>
                        <div class="h-1.5 bg-gray-200 rounded w-full"></div>
                    </div>
                    <div class="flex items-center gap-2">
                         <div class="w-3 h-3 bg-gray-300 rounded-sm"></div>
                        <div class="h-1.5 bg-gray-200 rounded w-full"></div>
                    </div>
                </div>

                <div class="mt-4 bg-white p-2 rounded border border-gray-200 flex items-start gap-2 shadow-sm">
                    <div class="text-green-600 mt-0.5">
                        <svg xmlns="http://www.w3.org/2000/svg" width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"><polyline points="20 6 9 17 4 12"/></svg>
                    </div>
                    <div>
                        <p class="text-[10px] font-medium">Patient meets the criteria for antibiotics</p>
                    </div>
                </div>
            </div>
        </div>
      </div>
    </div>
  </div>
</section>
