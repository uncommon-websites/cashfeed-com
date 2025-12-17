<section class="relative h-[500px] flex items-center justify-center overflow-hidden">
    <!-- Background Landscape -->
    <div class="absolute inset-0 z-0">
        <!-- Sky -->
        <div class="absolute inset-0 bg-gradient-to-b from-blue-50 via-blue-100 to-blue-200 h-2/3"></div>
        
        <!-- Hills (CSS Shapes) -->
        <div class="absolute bottom-0 left-0 right-0 h-1/3 bg-[#8ba88e]"></div> <!-- Base green -->
        
        <!-- Back hills -->
        <div class="absolute bottom-1/4 left-0 w-full h-64 bg-[#7a9980] rounded-[50%] transform scale-150 translate-y-12 opacity-80"></div>
        <div class="absolute bottom-1/4 right-0 w-full h-64 bg-[#6b8c72] rounded-[50%] transform scale-150 translate-y-24 opacity-80"></div>
        
        <!-- Front hills -->
        <div class="absolute bottom-0 left-[-20%] w-[140%] h-48 bg-[#4a6b50] rounded-[100%] transform translate-y-10"></div>
        
        <!-- Trees/Details (Abstract) -->
        <div class="absolute bottom-10 left-10 w-4 h-12 bg-[#2d4232] rounded-full opacity-60"></div>
        <div class="absolute bottom-16 left-24 w-6 h-16 bg-[#2d4232] rounded-full opacity-60"></div>
        <div class="absolute bottom-12 right-32 w-5 h-14 bg-[#2d4232] rounded-full opacity-60"></div>
        
        <!-- Mist/Fog -->
        <div class="absolute bottom-0 left-0 right-0 h-32 bg-gradient-to-t from-white/20 to-transparent"></div>
    </div>

    <!-- Content -->
    <div class="relative z-10 text-center max-w-4xl mx-auto px-4">
        <h2 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8 drop-shadow-sm">
            A month of invoices,<br />paid in seconds
        </h2>
        
        <div class="flex flex-col items-center gap-3">
            <button class="bg-gray-900 text-white px-8 py-3.5 rounded-full font-medium hover:bg-gray-800 transition-colors shadow-lg hover:shadow-xl transform hover:-translate-y-0.5 duration-200">
                Get started for free
            </button>
            <span class="text-xs text-gray-700 font-medium">No credit card required</span>
        </div>
    </div>
</section>
