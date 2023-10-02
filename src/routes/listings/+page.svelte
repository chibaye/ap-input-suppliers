<script>
    import rows from './rows.json'
    import columns from './columns.json'
</script>

<svelte:head>
    <title>Product Listings</title>
    <meta name='description' content='Product Listings'/>
</svelte:head>

<div>
    <div class='flex items-center'>
        <div class='flex-auto mb-7'>
            <h1 class='text-xl font-semibold leading-6 text-gray-900'>Product Listings</h1>
            <p class='mt-2 text-sm text-gray-700'>
                A list of all the products in your account including their name, views, offers and matches.
            </p>
        </div>
        <div class='ml-16 flex-none'>
            <button type='button' class='flex items-center py-1.5 px-3 text-md bg-gray-100 text-center text-gray-900 focus:outline-none rounded-md border border-gray-200 hover:bg-gray-100 hover:text-gray-900 placeholder:text-gray-400 focus:ring-1 focus:ring-inset focus:ring-gray-600'>
                <span class='-ml-1 font-extrabold'>＋</span>
                <span class='ml-1 font-semibold text-sm text-gray-600'>New Product</span>
            </button>
        </div>
    </div>
    <div class='bg-white shadow-md rounded-lg overflow-hidden'>
        <div class='p-4 flex flex-col h-[calc(100vh-16rem)]'>
            <div class='grid grid-cols-12 gap-3 mb-4'>
                <div class='col-span-7 flex items-center w-full rounded-md border-0 py-1.5 px-3 text-sm text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus-within:ring-1 focus-within:ring-inset focus-within:ring-gray-600'>
                    <svg class=' w-4 h-4 text-gray-400 dark:text-gray-400' aria-hidden='true' xmlns='http://www.w3.org/2000/svg' fill='none' viewBox='0 0 20 20'>
                        <path stroke='currentColor' stroke-linecap='round' stroke-linejoin='round' stroke-width='2' d='m19 19-4-4m0-7A7 7 0 1 1 1 8a7 7 0 0 1 14 0Z'/>
                    </svg>
                    <input type='email' name='email' class='ml-2 w-full focus:outline-none parent-focus:outline' placeholder='Search...'>
                </div>
                <button class='col-span-2 block w-full rounded-md py-1.5 px-4 bg-gray-100 text-sm text-start text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-1 focus:ring-inset focus:ring-gray-600'>Filter</button>
                <button class='col-span-3 block w-full rounded-md py-1.5 px-4 bg-gray-100 text-sm text-start text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-1 focus:ring-inset focus:ring-gray-600'>Aug 07, 2023 – Sep 06, 2023</button>
            </div>

            <div class='flex-grow overflow-auto inline-block min-w-full align-middle'>
                <table class='min-w-full'>
                    <thead>
                    <tr>
                        {#each columns as col}
                            <th scope='col' class='bg-gray-100 sticky top-0 px-3 py-2 text-left text-sm font-semibold text-gray-900'>{col.label}</th>
                        {/each}
                    </tr>
                    </thead>
                    <tbody class='bg-white'>
                    {#each rows as row}
                        <tr class='even:bg-gray-50'>
                            {#each columns as col}
                                <td class='whitespace-nowrap px-3 py-2 text-sm text-gray-500'>{row[col.id]}</td>
                            {/each}
                        </tr>
                    {/each}
                    </tbody>
                </table>
            </div>
        </div>
    </div>
</div>