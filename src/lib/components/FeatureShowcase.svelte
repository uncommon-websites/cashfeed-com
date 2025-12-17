<script>
    import { Check, X, Plus, Clock } from 'lucide-svelte';
</script>

<section class="py-24 bg-gray-50 overflow-hidden">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-20 max-w-3xl mx-auto">
            <h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-6">
                This is how easy invoicing can be
            </h2>
            <p class="text-lg text-gray-600">
                Creating and sending invoices in less than 5 clicks – that's half the number of clicks compared to any other tool. But now you can also receive, approve, and pay invoices all in one place: quickly and efficiently.
            </p>
        </div>

        <div class="space-y-32">
            <!-- Feature 1: Automatic Retrieval -->
            <div class="flex flex-col lg:flex-row items-center gap-16">
                <div class="flex-1 w-full max-w-lg relative">
                    <!-- UI Mockup -->
                    <div class="bg-white rounded-2xl shadow-xl border border-gray-200 p-6 relative z-10">
                        <div class="absolute -top-3 right-8 bg-white border border-gray-200 shadow-sm text-xs font-medium px-2 py-1 rounded-md text-gray-500">
                            2 duplicates detected
                        </div>
                        
                        <div class="space-y-3">
                            {#each [
                                { name: 'Zoom', status: 'Due', amount: '€149', color: 'bg-blue-500' },
                                { name: 'Slack', status: 'Due', amount: '€535', color: 'bg-purple-500' },
                                { name: 'Linear', status: 'Due', amount: '€230', color: 'bg-indigo-500' },
                                { name: 'Loom', status: 'Paid', amount: '€420', color: 'bg-pink-500', paid: true },
                                { name: 'Apple', status: 'Due', amount: '€749', color: 'bg-gray-800' }
                            ] as item}
                            <div class="flex items-center justify-between p-3 rounded-lg border border-gray-100 hover:bg-gray-50 transition-colors">
                                <div class="flex items-center gap-3">
                                    <div class="w-6 h-6 {item.color} rounded flex items-center justify-center text-white text-[10px]">
                                        {item.name[0]}
                                    </div>
                                    <span class="text-sm font-medium text-gray-900">{item.name}</span>
                                </div>
                                <div class="flex items-center gap-4">
                                    <span class="text-[10px] font-bold {item.paid ? 'text-green-500' : 'text-orange-500'} bg-{item.paid ? 'green' : 'orange'}-50 px-1.5 py-0.5 rounded">
                                        {item.status}
                                    </span>
                                    <span class="text-sm font-medium text-gray-900 w-12 text-right">{item.amount}</span>
                                </div>
                            </div>
                            {/each}
                        </div>

                        <!-- Floating Badge -->
                        <div class="absolute -bottom-4 left-1/2 -translate-x-1/2 bg-cashfeed-dark text-white px-4 py-2 rounded-full text-xs font-medium shadow-lg flex items-center gap-2">
                            <div class="w-2 h-2 bg-green-400 rounded-full animate-pulse"></div>
                            New invoices detected
                        </div>
                        
                        <!-- Connecting line visual -->
                        <div class="absolute top-1/2 -left-12 w-12 h-px border-t border-dashed border-gray-300 hidden lg:block"></div>
                        <div class="absolute top-1/2 -left-12 text-xs text-gray-400 bg-gray-50 px-1 -translate-y-1/2 hidden lg:block">5 invoices retrieved</div>
                    </div>
                </div>
                
                <div class="flex-1">
                    <h3 class="text-2xl font-bold text-gray-900 mb-4">Automatic retrieval</h3>
                    <p class="text-gray-600 mb-6">
                        Cashfeed finds invoices in your mailbox and that of your colleagues, but also behind portals.
                    </p>
                    <p class="text-gray-600 mb-8">
                        We read them out, remove duplicates, and prepare everything for payment with one click.
                    </p>
                    <div class="flex items-center gap-4 text-sm text-gray-500">
                        Works with: 
                        <div class="flex gap-2">
                            <div class="w-5 h-5 bg-blue-600 rounded-sm"></div>
                            <div class="w-5 h-5 bg-red-500 rounded-sm"></div>
                            <div class="w-5 h-5 bg-yellow-400 rounded-sm"></div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Feature 2: Automatic Approvals -->
            <div class="flex flex-col lg:flex-row-reverse items-center gap-16">
                <div class="flex-1 w-full max-w-lg relative">
                    <div class="bg-white rounded-2xl shadow-xl border border-gray-200 p-6 relative z-10">
                        <div class="space-y-4">
                            {#each [
                                { name: 'Nicolas Cage', role: 'Approval pending' },
                                { name: 'Richard Miles', role: 'Approval pending' },
                                { name: 'Grace Turner', role: 'Approval pending' }
                            ] as person}
                            <div class="flex items-center justify-between p-3 border-b border-gray-50 last:border-0">
                                <div class="flex items-center gap-3">
                                    <div class="w-10 h-10 bg-gray-200 rounded-full overflow-hidden">
                                        <!-- Placeholder Avatar -->
                                        <svg class="w-full h-full text-gray-400" fill="currentColor" viewBox="0 0 24 24">
                                            <path d="M24 20.993V24H0v-2.996A14.977 14.977 0 0112.004 15c4.904 0 9.26 2.354 11.996 5.993zM16.002 8.999a4 4 0 11-8 0 4 4 0 018 0z" />
                                        </svg>
                                    </div>
                                    <div>
                                        <div class="text-sm font-medium text-gray-900">{person.name}</div>
                                        <div class="text-xs text-gray-500">{person.role}</div>
                                    </div>
                                </div>
                                <div class="flex gap-2">
                                    <button class="px-3 py-1.5 text-xs font-medium text-gray-600 hover:bg-gray-100 rounded-full border border-gray-200">Decline</button>
                                    <button class="px-3 py-1.5 text-xs font-medium text-white bg-cashfeed-dark hover:bg-gray-800 rounded-full">Approve</button>
                                </div>
                            </div>
                            {/each}
                        </div>

                        <!-- Floating Badge -->
                        <div class="absolute -bottom-4 right-8 bg-cashfeed-dark text-white px-4 py-2 rounded-full text-xs font-medium shadow-lg flex items-center gap-2">
                            <div class="w-5 h-5 bg-white/20 rounded-full flex items-center justify-center text-[10px]">3</div>
                            3 invoices are waiting for your approval
                        </div>

                        <!-- Purple dot annotation -->
                        <div class="absolute top-1/3 -right-3 w-3 h-3 bg-purple-500 rounded-full border-2 border-white"></div>
                        <div class="absolute top-1/3 -right-16 bg-purple-500 text-white text-[10px] px-2 py-0.5 rounded-full">Dennis</div>
                    </div>
                </div>

                <div class="flex-1">
                    <h3 class="text-2xl font-bold text-gray-900 mb-4">Never pay blindly again with automatic approvals</h3>
                    <p class="text-gray-600 mb-6">
                        Our AI agent automatically submits each invoice for approval to the right person. In Slack, Teams, or via email — wherever they prefer.
                    </p>
                    <p class="text-gray-600">
                        You will now receive approval with just 1 click, without delays, without doubt.
                    </p>
                </div>
            </div>

            <!-- Feature 3: Bulk Payments -->
            <div class="flex flex-col lg:flex-row items-center gap-16">
                <div class="flex-1 w-full max-w-lg relative">
                    <div class="bg-white rounded-2xl shadow-xl border border-gray-200 p-8 relative z-10">
                        <div class="absolute -top-3 left-6 bg-orange-50 text-orange-600 border border-orange-100 px-3 py-1 rounded-full text-xs font-medium flex items-center gap-1">
                            <Clock size={12} /> Scheduled payment in 2h 4m
                        </div>

                        <div class="space-y-4 mt-4">
                            {#each [
                                { id: '#24-244', name: 'Slack', amount: '€365.00' },
                                { id: '#123-424', name: 'Linear', amount: '€274.00' },
                                { id: '#492-471', name: 'Loom', amount: '€546.00' },
                                { id: '#8974', name: 'Apple', amount: '€420.00' }
                            ] as item, i}
                            <div class="flex items-center justify-between p-2 {i > 1 ? 'opacity-40' : ''}">
                                <div class="flex items-center gap-3">
                                    <div class="w-4 h-4 rounded border border-gray-300 bg-cashfeed-dark flex items-center justify-center">
                                        {#if i < 2}<Check size={10} class="text-white" />{/if}
                                    </div>
                                    <span class="text-sm text-gray-500 font-mono">{item.id}</span>
                                    <span class="text-sm font-medium text-gray-900">{item.name}</span>
                                </div>
                                <span class="text-sm font-medium text-gray-900">{item.amount}</span>
                            </div>
                            {/each}
                            
                            <div class="pt-4 border-t border-gray-100 flex justify-between items-center">
                                <span class="text-sm font-medium text-gray-500">Total</span>
                                <span class="text-lg font-bold text-gray-900">€639.00</span>
                            </div>

                            <button class="w-full bg-cashfeed-dark text-white py-3 rounded-lg font-medium shadow-lg hover:bg-gray-800 transition-colors relative overflow-hidden">
                                Pay 2 invoices
                                <!-- Green success bubble -->
                                <div class="absolute -bottom-2 -right-2 w-8 h-8 bg-cashfeed-green rounded-full"></div>
                            </button>
                            
                             <!-- Green bubble annotation -->
                             <div class="absolute -bottom-2 -right-4 bg-cashfeed-green text-white text-xs px-2 py-1 rounded-full">Stijn</div>
                        </div>
                    </div>
                    
                    <!-- Background card effect -->
                    <div class="absolute top-4 left-4 right-4 bottom-0 bg-gray-50 rounded-2xl -z-10 border border-gray-200 transform rotate-3"></div>
                </div>

                <div class="flex-1">
                    <h3 class="text-2xl font-bold text-gray-900 mb-4">Bulk payments you can rely on</h3>
                    <p class="text-gray-600 mb-6">
                        Pay all outstanding invoices with one click or schedule them for the next payment day. Cashfeed alerts you to new suppliers, anomalies, and potential duplicates.
                    </p>
                    <p class="text-gray-600">
                        This ensures that each supplier is paid correctly.
                    </p>
                </div>
            </div>
        </div>
    </div>
</section>
