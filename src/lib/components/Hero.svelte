<script>
    import { Check, Search, Plus, Bell, Upload, ArrowUpRight, ArrowDownLeft, FileText, MoreHorizontal } from 'lucide-svelte';
</script>

<section class="relative pt-16 pb-32 overflow-hidden bg-gradient-to-b from-white to-gray-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center relative z-10">
        
        <!-- Tagline -->
        <div class="inline-flex items-center gap-2 bg-white border border-gray-200 rounded-full px-4 py-1.5 mb-8 shadow-sm">
            <div class="w-4 h-4 rounded-full border border-gray-300 flex items-center justify-center">
                <div class="w-2 h-2 bg-gray-300 rounded-full"></div>
            </div>
            <span class="text-sm text-gray-600 font-medium">Comply with PEPPOL in less than 2 minutes</span>
            <span class="text-lg leading-none">🇧🇪</span>
        </div>

        <!-- Headline -->
        <h1 class="text-5xl md:text-6xl font-bold tracking-tight text-gray-900 mb-6 max-w-4xl mx-auto leading-tight">
            A month of invoices,<br />paid in seconds
        </h1>

        <!-- Subheadline -->
        <p class="text-xl text-gray-600 mb-10 max-w-2xl mx-auto leading-relaxed">
            Sending and receiving (E-)invoices faster than ever. Cashfeed collects them, lets you pay with one click, and matches purchases with the correct ledger account. Save hours each month.
        </p>

        <!-- CTA -->
        <div class="flex flex-col items-center gap-3 mb-20">
            <button class="bg-gray-900 text-white px-8 py-3.5 rounded-full font-medium hover:bg-gray-800 transition-colors shadow-lg hover:shadow-xl transform hover:-translate-y-0.5 duration-200">
                Get started for free
            </button>
            <span class="text-xs text-gray-500">No credit card required</span>
        </div>

        <!-- Hero Image / UI Mockup -->
        <div class="relative w-full max-w-6xl mx-auto perspective-1000">
            <!-- Main Dashboard Card -->
            <div class="bg-white rounded-xl shadow-2xl border border-gray-200 overflow-hidden text-left relative z-10 transform transition-transform duration-500 [transform:rotateX(2deg)] hover:[transform:rotateX(0deg)]">
                <div class="flex h-[600px]">
                    <!-- Sidebar -->
                    <div class="w-64 border-r border-gray-100 bg-gray-50/50 p-4 hidden md:block">
                        <div class="flex items-center gap-2 mb-6 px-2">
                            <div class="w-6 h-6 bg-gray-900 rounded"></div>
                            <span class="font-bold text-sm">StarApps</span>
                        </div>
                        
                        <div class="relative mb-6">
                            <Search size={14} class="absolute left-3 top-2.5 text-gray-400" />
                            <input type="text" placeholder="Search" class="w-full bg-white border border-gray-200 rounded-lg pl-9 py-2 text-sm focus:outline-none focus:border-gray-300" />
                        </div>

                        <div class="space-y-1">
                            <div class="flex items-center justify-between px-3 py-2 bg-white rounded-lg shadow-sm border border-gray-100">
                                <div class="flex items-center gap-3">
                                    <div class="w-4 h-4 rounded border border-gray-300"></div>
                                    <span class="text-sm font-medium text-gray-900">Overview</span>
                                </div>
                                <span class="bg-orange-100 text-orange-600 text-xs font-bold px-1.5 py-0.5 rounded">7</span>
                            </div>
                            {#each ['Incoming', 'Outgoing', 'Transactions'] as item}
                            <div class="flex items-center gap-3 px-3 py-2 text-gray-600 hover:bg-gray-100 rounded-lg cursor-pointer">
                                <div class="w-4 h-4 rounded border border-gray-300"></div>
                                <span class="text-sm">{item}</span>
                            </div>
                            {/each}
                        </div>

                        <div class="mt-8 px-3">
                            <div class="bg-white p-4 rounded-xl border border-gray-200 shadow-sm text-center">
                                <div class="w-10 h-10 bg-gray-50 rounded-full flex items-center justify-center mx-auto mb-3">
                                    <Upload size={16} class="text-gray-400" />
                                </div>
                                <p class="text-xs font-medium text-gray-900 mb-1">Add documents</p>
                                <p class="text-[10px] text-gray-500 mb-3">Add documents by forwarding emails to:</p>
                                <div class="bg-gray-50 rounded px-2 py-1 text-[10px] text-gray-600 truncate">starapps@cashfeed.com</div>
                            </div>
                        </div>
                    </div>

                    <!-- Main Content -->
                    <div class="flex-1 p-8 bg-white overflow-y-auto">
                        <div class="flex justify-between items-end mb-8">
                            <div>
                                <h2 class="text-xl font-bold text-gray-900 mb-1">Overview</h2>
                                <p class="text-sm text-gray-500">These <span class="font-bold text-gray-900">7 items</span> require your attention</p>
                            </div>
                        </div>

                        <div class="space-y-0">
                            <!-- List Header -->
                            <div class="grid grid-cols-12 gap-4 px-4 py-2 text-xs font-medium text-gray-400 border-b border-gray-100">
                                <div class="col-span-4">NAME</div>
                                <div class="col-span-4">STATUS</div>
                                <div class="col-span-4 text-right">AMOUNT</div>
                            </div>

                            <!-- Items -->
                            {#each [
                                { name: 'Telenet', sub: '1 Feb - Internet subscription', amount: '€ 749', status: 'Processing' },
                                { name: 'Paypal', sub: 'Transaction from Paypal', amount: '', status: 'Document missing', warning: true },
                                { name: 'Colruyt', sub: '12 Jan - Project 452', amount: '€ 1.000,00', status: 'Processing' },
                                { name: 'Framer', sub: '6 Jan - Branding Project', amount: '€ 1.236,20', status: 'Processing' },
                                { name: 'FixForm', sub: '4 Jan - Contract renewal', amount: '€ 1.540,00', status: 'Processing' },
                                { name: 'Bizzy', sub: '1 Jan - Contract renewal', amount: '€ 600,00', status: 'Processing' },
                                { name: 'Introw', sub: '1 Jan - Contract renewal', amount: '€ 10,00', status: 'Processing' }
                            ] as item}
                            <div class="grid grid-cols-12 gap-4 px-4 py-4 border-b border-gray-50 items-center hover:bg-gray-50 transition-colors group">
                                <div class="col-span-4 flex items-center gap-3">
                                    <div class="w-8 h-8 rounded bg-gray-100 flex items-center justify-center text-xs font-bold text-gray-500">
                                        {item.name[0]}
                                    </div>
                                    <div>
                                        <div class="text-sm font-medium text-gray-900">{item.name}</div>
                                        <div class="text-xs text-gray-500">{item.sub}</div>
                                    </div>
                                </div>
                                <div class="col-span-4">
                                    {#if item.warning}
                                        <span class="inline-flex items-center px-2 py-1 rounded-full text-xs font-medium bg-orange-50 text-orange-600">
                                            {item.status}
                                        </span>
                                    {:else}
                                         <span class="text-xs text-gray-400 group-hover:hidden">
                                            <ArrowDownLeft size={12} class="inline mr-1" /> {item.status}
                                        </span>
                                    {/if}
                                </div>
                                <div class="col-span-4 text-right">
                                    <div class="text-sm font-medium text-gray-900">{item.amount}</div>
                                </div>
                            </div>
                            {/each}
                        </div>
                    </div>

                    <!-- Right Panel (Floating) -->
                    <div class="w-80 bg-white border-l border-gray-100 p-6 hidden lg:block absolute right-0 top-0 bottom-0 shadow-[-10px_0_30px_-10px_rgba(0,0,0,0.05)]">
                        <h3 class="text-sm font-medium text-gray-900 mb-4">These 2 items require your attention</h3>
                        
                        <div class="space-y-3">
                            <div class="p-3 bg-white border border-gray-200 rounded-lg shadow-sm hover:border-gray-300 transition-colors cursor-pointer">
                                <div class="flex items-center justify-between mb-2">
                                    <div class="flex items-center gap-2">
                                        <div class="w-6 h-6 bg-black rounded flex items-center justify-center text-white text-xs">A</div>
                                        <span class="text-sm font-medium">Apple</span>
                                    </div>
                                    <span class="text-sm font-bold">€749</span>
                                </div>
                                <div class="flex justify-between items-center text-xs">
                                    <span class="text-gray-500">Due today</span>
                                </div>
                            </div>

                            <div class="p-3 bg-white border border-red-200 rounded-lg shadow-sm bg-red-50/30 cursor-pointer">
                                <div class="flex items-center justify-between mb-2">
                                    <div class="flex items-center gap-2">
                                        <div class="w-6 h-6 bg-purple-600 rounded flex items-center justify-center text-white text-xs">S</div>
                                        <span class="text-sm font-medium">Slack</span>
                                    </div>
                                    <span class="text-sm font-bold">€219</span>
                                </div>
                                <div class="flex justify-between items-center text-xs">
                                    <span class="bg-red-100 text-red-600 px-1.5 py-0.5 rounded font-medium">Overdue</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Decorative Elements behind -->
             <div class="absolute -top-10 -left-10 w-64 h-64 bg-green-200 rounded-full mix-blend-multiply filter blur-3xl opacity-20 animate-blob"></div>
             <div class="absolute -top-10 -right-10 w-64 h-64 bg-purple-200 rounded-full mix-blend-multiply filter blur-3xl opacity-20 animate-blob animation-delay-2000"></div>
        </div>
    </div>
</section>

<style>
    .perspective-1000 {
        perspective: 1000px;
    }
</style>
