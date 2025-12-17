<script>
    import { Check, X, Lock, Globe, Code, RefreshCw } from 'lucide-svelte';

    let invoices = 250;
    let simpleInvoicing = true;
    let approvals = true;
    let accounting = false;

    $: basePrice = (invoices / 10) * 3.5; // Dummy formula
    $: total = 87.50; // Fixed for visual purposes as per screenshot, but could be dynamic
    
    // The screenshot shows 87.50 for 250 invoices with Simple Invoicing + Approvals selected.
    // Let's just hardcode the visual state to match the screenshot 1:1 first, or make it interactive?
    // "Recreate the website in the screenshot 1:1" usually implies visual fidelity.
    // I'll make the slider movable but maybe just keep the price static or simple logic.
    
    const featuresIncluded = [
        'Create and send invoices',
        'Basic invoice management',
        'Email support',
        'Scan receipts via WhatsApp',
        'Auto Invoice retrieval',
        '1 click payments'
    ];

    const featuresNotIncluded = [
        'Approval workflows via Slack en MS teams',
        'Custom approval rules',
        'Add multiple organisations',
        'Fully automated invoice workflows',
        'Intelligent data extraction',
        'Real-time categorization',
        'Integrates with your accounting software',
        'Advanced analytics',
        'Priority customer support'
    ];
</script>

<section class="py-24 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="mb-16">
            <h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4">
                Pay only for what you need
            </h2>
            <p class="text-lg text-gray-600">
                With dynamic pricing that grows with your company
            </p>
        </div>

        <div class="bg-gray-50 rounded-3xl p-8 md:p-12 mb-20">
            <div class="flex flex-col lg:flex-row gap-16">
                <!-- Left: Calculator -->
                <div class="flex-1 space-y-8">
                    <div>
                        <div class="flex justify-between items-center mb-4">
                            <span class="text-sm font-medium text-gray-900">I process <span class="font-bold">250</span> invoices per month</span>
                        </div>
                        <div class="relative h-2 bg-gray-200 rounded-full mb-2">
                            <div class="absolute top-0 left-0 h-full bg-gray-900 rounded-full" style="width: 50%"></div>
                            <div class="absolute top-1/2 -translate-y-1/2 left-1/2 w-6 h-6 bg-white border-4 border-gray-900 rounded-full shadow cursor-pointer"></div>
                        </div>
                        <div class="flex justify-between text-xs text-gray-400">
                            <span>10</span>
                            <span>125</span>
                            <span>250</span>
                            <span>325</span>
                            <span>500</span>
                        </div>
                    </div>

                    <div class="flex items-baseline gap-2">
                        <span class="text-4xl font-bold text-gray-900">€87.50</span>
                        <span class="text-gray-500">/month</span>
                    </div>

                    <div class="space-y-4">
                        <p class="text-sm font-medium text-gray-900">Select your modules</p>
                        
                        <div class="bg-white border border-gray-200 rounded-xl p-4 flex items-center justify-between cursor-pointer ring-1 ring-gray-900">
                            <div class="flex items-center gap-3">
                                <div class="w-5 h-5 rounded border border-gray-300 flex items-center justify-center">
                                    <div class="w-3 h-3 bg-gray-900 rounded-sm"></div>
                                </div>
                                <div>
                                    <div class="text-sm font-bold text-gray-900">Simple invoicing</div>
                                    <div class="text-xs text-gray-500">The most user friendly invoicing</div>
                                </div>
                            </div>
                            <div class="bg-gray-900 text-white rounded p-0.5">
                                <Check size={12} />
                            </div>
                        </div>

                        <div class="bg-white border border-gray-200 rounded-xl p-4 flex items-center justify-between cursor-pointer">
                            <div class="flex items-center gap-3">
                                <div class="w-5 h-5 rounded border border-gray-300 flex items-center justify-center bg-gray-900 text-white">
                                    <Check size={12} />
                                </div>
                                <div>
                                    <div class="text-sm font-bold text-gray-900">Approvals</div>
                                    <div class="text-xs text-gray-500">Implement approval workflows for invoicing.</div>
                                </div>
                            </div>
                        </div>

                        <div class="bg-white border border-gray-200 rounded-xl p-4 flex items-center justify-between cursor-pointer opacity-70">
                            <div class="flex items-center gap-3">
                                <div class="w-5 h-5 rounded border border-gray-300 flex items-center justify-center">
                                    <RefreshCw size={12} class="text-gray-400" />
                                </div>
                                <div>
                                    <div class="text-sm font-bold text-gray-900">Accounting automation</div>
                                    <div class="text-xs text-gray-500">Save hours weekly with automation.</div>
                                </div>
                            </div>
                             <div class="w-4 h-4 rounded border border-gray-300"></div>
                        </div>
                    </div>

                    <div class="pt-4">
                        <button class="w-full bg-gray-900 text-white py-3.5 rounded-full font-medium hover:bg-gray-800 transition-colors mb-3">
                            Get started for free
                        </button>
                        <p class="text-center text-xs text-gray-500">No credit card required</p>
                    </div>
                </div>

                <!-- Right: Features -->
                <div class="flex-1 border-l border-gray-200 pl-0 lg:pl-16 pt-8 lg:pt-0">
                    <div class="mb-8">
                        <h4 class="text-xs font-bold text-gray-900 uppercase tracking-wider mb-4">FEATURES INCLUDED</h4>
                        <ul class="space-y-3">
                            {#each featuresIncluded as feature}
                            <li class="flex items-center gap-3 text-sm text-gray-700">
                                <div class="w-4 h-4 rounded-full bg-green-500 flex items-center justify-center flex-shrink-0">
                                    <Check size={10} class="text-white" />
                                </div>
                                {feature}
                            </li>
                            {/each}
                        </ul>
                    </div>

                    <div>
                        <h4 class="text-xs font-bold text-gray-500 uppercase tracking-wider mb-4">NOT INCLUDED</h4>
                        <ul class="space-y-3">
                            {#each featuresNotIncluded as feature}
                            <li class="flex items-center gap-3 text-sm text-gray-400">
                                <X size={14} />
                                {feature}
                            </li>
                            {/each}
                        </ul>
                    </div>
                </div>
            </div>
        </div>

        <!-- Trust Badges -->
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8 border-t border-gray-100 pt-16">
            <div class="flex flex-col gap-3">
                <Lock size={20} class="text-gray-900" />
                <h3 class="font-bold text-gray-900">Bank-grade security</h3>
                <p class="text-sm text-gray-600 leading-relaxed">
                    Your data and payments are protected with encryption and access controls.
                </p>
            </div>
            <div class="flex flex-col gap-3">
                <Globe size={20} class="text-gray-900" />
                <h3 class="font-bold text-gray-900">PEPPOL integrated</h3>
                <p class="text-sm text-gray-600 leading-relaxed">
                    Send and receive e-invoices via PEPPOL, compliant and future-ready.
                </p>
            </div>
            <div class="flex flex-col gap-3">
                <Code size={20} class="text-gray-900" />
                <h3 class="font-bold text-gray-900">API</h3>
                <p class="text-sm text-gray-600 leading-relaxed">
                    Connect Cashfeed to your systems. Build custom integrations.
                </p>
            </div>
        </div>
    </div>
</section>
