<script>
    import { Instagram, Linkedin } from 'lucide-svelte';
</script>

<footer class="bg-gray-50 py-12 border-t border-gray-200">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col md:flex-row justify-between items-center gap-6">
        <div class="text-xs text-gray-500 text-center md:text-left">
            <p>2025 Cashfeed BV. All rights reserved.</p>
            <p>Dok-Noord 4D 101, 9000 Gent, Belgium.</p>
            <p>BE1020118217</p>
        </div>

        <div class="flex gap-6 text-xs text-gray-600 font-medium">
            <a href="/" class="hover:text-gray-900">Privacy policy</a>
            <a href="/" class="hover:text-gray-900">Terms & conditions</a>
        </div>

        <div class="flex gap-4">
            <a href="/" class="text-gray-400 hover:text-gray-900 transition-colors">
                <Instagram size={20} />
            </a>
            <a href="/" class="text-gray-400 hover:text-gray-900 transition-colors">
                <Linkedin size={20} />
            </a>
        </div>
    </div>
</footer>
