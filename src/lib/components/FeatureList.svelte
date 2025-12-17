<script>
    import { Check, Mail, RefreshCw, CheckCircle, CreditCard, LayoutGrid, Plug, Clock, BarChart3 } from 'lucide-svelte';

    const features = [
        { icon: Mail, text: "Scrape invoices from your inbox" },
        { icon: LayoutGrid, text: "Track everything in one view" },
        { icon: RefreshCw, text: "Auto-match in your accounting" },
        { icon: Plug, text: "Connect your existing tools" },
        { icon: CheckCircle, text: "Smart and fast payment approvals" },
        { icon: Clock, text: "Save hours per week" },
        { icon: CreditCard, text: "Pay with context and overview" },
        { icon: BarChart3, text: "Scalable billing" }
    ];
</script>

<section class="py-24 bg-white relative overflow-hidden">
    <!-- Abstract Visual Left -->
    <div class="absolute left-0 top-1/2 -translate-y-1/2 -translate-x-1/2 w-64 h-96 opacity-50 hidden lg:block">
        <div class="bg-gray-50 border border-gray-100 rounded-xl p-4 transform -rotate-12 shadow-lg w-full h-full">
            <div class="h-4 w-24 bg-gray-200 rounded mb-4"></div>
            <div class="space-y-2">
                <div class="h-2 w-full bg-gray-100 rounded"></div>
                <div class="h-2 w-full bg-gray-100 rounded"></div>
                <div class="h-2 w-2/3 bg-gray-100 rounded"></div>
            </div>
        </div>
    </div>

    <!-- Abstract Visual Right -->
    <div class="absolute right-0 top-1/2 -translate-y-1/2 translate-x-1/2 w-64 h-96 opacity-50 hidden lg:block">
        <div class="bg-white border border-gray-100 rounded-xl p-4 transform rotate-12 shadow-lg w-full h-full">
            <div class="flex justify-between mb-4">
                <div class="h-8 w-8 bg-green-100 rounded-full"></div>
                <div class="h-4 w-16 bg-gray-100 rounded"></div>
            </div>
            <div class="space-y-3">
                <div class="h-2 w-full bg-gray-50 rounded"></div>
                <div class="h-2 w-full bg-gray-50 rounded"></div>
            </div>
        </div>
    </div>

    <div class="max-w-3xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
        <div class="text-center mb-16">
            <h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-6">
                Invoices are costing you time and money
            </h2>
            <p class="text-lg text-gray-600 leading-relaxed">
                With Cashfeed, invoices are one less worry. No more searching, retyping, or paying blindly. We take care of finding, reading, matching, and preparing for payment.
            </p>
            <p class="text-lg text-gray-600 leading-relaxed mt-4">
                So you and your team can focus on what really requires your attention.
            </p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 gap-x-8 gap-y-6">
            {#each features as feature}
            <div class="flex items-center gap-4">
                <div class="flex-shrink-0 w-8 h-8 rounded-full bg-cashfeed-green flex items-center justify-center text-white">
                    <feature.icon size={16} strokeWidth={2.5} />
                </div>
                <span class="text-gray-900 font-medium">{feature.text}</span>
            </div>
            {/each}
        </div>
    </div>
</section>
