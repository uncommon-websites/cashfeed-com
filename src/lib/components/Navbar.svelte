<script>
    import { ChevronDown } from 'lucide-svelte';
</script>

<div class="bg-cashfeed-dark text-white text-center py-2 text-sm font-medium">
    <a href="/" class="hover:underline flex items-center justify-center gap-1">
        Cashfeed has raised 1.3M euro to make e-invoicing smarter
        <span class="text-xs">›</span>
    </a>
</div>

<nav class="sticky top-0 z-50 bg-white/90 backdrop-blur-sm border-b border-gray-100">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex justify-between items-center h-16">
            <!-- Logo -->
            <div class="flex-shrink-0 flex items-center gap-2">
                <div class="bg-cashfeed-green text-white w-8 h-8 rounded-lg flex items-center justify-center font-bold text-xl">C</div>
                <span class="font-bold text-xl tracking-tight text-gray-900">Cashfeed</span>
            </div>

            <!-- Desktop Menu -->
            <div class="hidden md:flex items-center space-x-8">
                <a href="/" class="text-gray-600 hover:text-gray-900 font-medium text-sm">About us</a>
                <a href="/" class="text-gray-600 hover:text-gray-900 font-medium text-sm">Pricing</a>
                <a href="/" class="text-gray-600 hover:text-gray-900 font-medium text-sm">Blog</a>
                <a href="/" class="text-gray-600 hover:text-gray-900 font-medium text-sm">Help</a>
            </div>

            <!-- Right Side -->
            <div class="hidden md:flex items-center space-x-4">
                <button class="flex items-center text-gray-600 hover:text-gray-900 text-sm font-medium">
                    EN <ChevronDown size={14} class="ml-1" />
                </button>
                <a href="/" class="text-gray-900 hover:text-gray-700 font-medium text-sm px-4 py-2 border border-gray-200 rounded-lg">
                    Login
                </a>
            </div>
        </div>
    </div>
</nav>
