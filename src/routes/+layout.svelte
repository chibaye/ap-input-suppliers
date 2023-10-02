<script>
    import '../app.css'
    import Button from '$widget/button.svelte'
    import Submenu from '$widget/submenu.svelte'
    import logo from '$lib/images/logo.png'
</script>

<div class='relative min-h-screen'>
    <nav class='relative bg-white h-16 flex items-center max-w-5xl m-auto  select-none'>
        <div class='flex-auto pr-6 flex items-center z-10 min-w-0'>
            <img class='h-12 my-2' src={logo} alt='AgriPredict'/>
        </div>
        <div class='links flex-auto z-10 min-w-0 flex items-center justify-end'>
            <div class='flex items-center space-x-2'>
                <div class='flex items-center'>
                    <Button>Feedback</Button>
                </div>
                <div class='flex items-center space-x-2.5'>
                    <a href='/help' class='text-sm text-gray-500 hover:text-gray-700'>Help & Support</a>
                </div>
                <div class='flex items-center space-x-2.5'>
                    <div class='relative inline-flex items-center justify-center w-8 h-8 overflow-hidden bg-white hover:bg-gray-100 border border-gray-100 hover:border-gray-200 rounded-full'>
                        <svg xmlns='http://www.w3.org/2000/svg' fill='none' viewBox='0 0 24 24' stroke-width='1.5' stroke='currentColor' class='w-5 h-5'>
                            <path stroke-linecap='round' stroke-linejoin='round' d='M14.857 17.082a23.848 23.848 0 005.454-1.31A8.967 8.967 0 0118 9.75v-.7V9A6 6 0 006 9v.75a8.967 8.967 0 01-2.312 6.022c1.733.64 3.56 1.085 5.455 1.31m5.714 0a24.255 24.255 0 01-5.714 0m5.714 0a3 3 0 11-5.714 0'/>
                        </svg>
                    </div>
                    <div class='relative inline-flex items-center justify-center w-8 h-8 overflow-hidden bg-gray-100 rounded-full dark:bg-gray-600'>
                        <span class='text-sm text-gray-600 dark:text-gray-300'>JL</span>
                    </div>
                </div>
            </div>
        </div>
    </nav>
    <Submenu/>
    <main class='bg-gray-50 w-full h-[calc(100vh-6.4rem)]'>
        <div class='relative flex flex-col max-w-5xl m-auto pt-8  container mx-auto font-sans'>
            <slot/>
        </div>
    </main>
</div>
