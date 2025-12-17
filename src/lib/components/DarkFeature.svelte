<script>
    import { RefreshCw } from 'lucide-svelte';
</script>

<section class="bg-cashfeed-dark py-24 overflow-hidden">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex flex-col lg:flex-row items-center gap-16">
            <div class="flex-1 text-white">
                <h2 class="text-3xl md:text-4xl font-bold mb-6">
                    Automatically match each invoice with the correct general ledger account
                </h2>
                <p class="text-gray-400 mb-8 text-lg leading-relaxed">
                    AI assigns the right ledger and cost center for every invoice and intuitively, so we didn't really have to explain that.
                </p>
                <p class="text-gray-400 mb-10 text-lg leading-relaxed">
                    Finished with manually splitting invoices to gain insight into your costs.
                </p>
                <button class="bg-white text-gray-900 px-8 py-3 rounded-full font-medium hover:bg-gray-100 transition-colors">
                    Get started for free
                </button>
            </div>

            <div class="flex-1 w-full max-w-xl">
                <div class="bg-white rounded-2xl p-6 relative h-[400px] flex items-center justify-center overflow-hidden">
                    <!-- Background Grid -->
                    <div class="absolute inset-0 grid grid-cols-6 grid-rows-6 gap-4 opacity-10 pointer-events-none">
                        {#each Array(36) as _}
                            <div class="border border-gray-300 rounded"></div>
                        {/each}
                    </div>

                    <!-- Diagram Container -->
                    <div class="relative w-full h-full flex items-center justify-between px-4">
                        
                        <!-- Left: Invoice -->
                        <div class="w-24 bg-white border border-gray-200 shadow-lg rounded-lg p-2 space-y-2 z-10">
                            <div class="h-2 w-12 bg-gray-200 rounded"></div>
                            <div class="h-1 w-full bg-gray-100 rounded"></div>
                            <div class="h-1 w-full bg-gray-100 rounded"></div>
                            <div class="h-1 w-2/3 bg-gray-100 rounded"></div>
                            <div class="mt-2 h-8 w-full bg-purple-50 rounded border border-purple-100 flex items-center justify-center">
                                <span class="text-[8px] text-purple-600 font-bold">2025-5625</span>
                            </div>
                        </div>

                        <!-- Middle: Processing -->
                        <div class="relative z-20">
                            <div class="w-12 h-12 bg-cashfeed-dark rounded-full flex items-center justify-center shadow-xl border-4 border-white">
                                <div class="animate-spin-slow">
                                    <RefreshCw size={20} class="text-white" />
                                </div>
                            </div>
                            <!-- Connecting Lines -->
                            <div class="absolute top-1/2 left-full w-16 h-px border-t-2 border-dashed border-green-400 -translate-y-1/2"></div>
                            <div class="absolute top-1/2 right-full w-16 h-px border-t-2 border-dashed border-gray-300 -translate-y-1/2"></div>
                        </div>

                        <!-- Right: Ledger -->
                        <div class="w-32 bg-white border border-gray-200 shadow-lg rounded-lg p-2 z-10">
                            <div class="flex gap-1 mb-2">
                                <div class="w-2 h-2 rounded-full bg-red-400"></div>
                                <div class="w-2 h-2 rounded-full bg-yellow-400"></div>
                                <div class="w-2 h-2 rounded-full bg-green-400"></div>
                            </div>
                            <div class="space-y-1">
                                <div class="h-4 w-full bg-gray-50 rounded flex items-center px-1">
                                    <div class="w-2 h-2 bg-purple-400 rounded-full mr-1"></div>
                                    <div class="h-1 w-10 bg-gray-200 rounded"></div>
                                </div>
                                <div class="h-4 w-full bg-gray-50 rounded flex items-center px-1">
                                    <div class="w-2 h-2 bg-gray-300 rounded-full mr-1"></div>
                                    <div class="h-1 w-12 bg-gray-200 rounded"></div>
                                </div>
                                <div class="h-4 w-full bg-gray-50 rounded flex items-center px-1 border border-green-200 bg-green-50">
                                    <div class="w-2 h-2 bg-green-500 rounded-full mr-1"></div>
                                    <div class="h-1 w-14 bg-green-200 rounded"></div>
                                </div>
                            </div>
                        </div>

                        <!-- Labels/Tags (Floating) -->
                        <div class="absolute top-10 right-20 bg-purple-600 text-white text-[10px] px-2 py-1 rounded-full shadow-lg">Cost center</div>
                        <div class="absolute top-20 right-32 bg-gray-400 text-white text-[10px] px-2 py-1 rounded-full shadow-lg">VAT</div>
                        <div class="absolute bottom-20 right-24 bg-green-500 text-white text-[10px] px-2 py-1 rounded-full shadow-lg">Ledger</div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>

<style>
    .animate-spin-slow {
        animation: spin 3s linear infinite;
    }
    @keyframes spin {
        from { transform: rotate(0deg); }
        to { transform: rotate(360deg); }
    }
</style>
