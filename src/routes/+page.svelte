<script>

</script>

<svelte:head>
	<title>Home</title>
	<meta name='description' content='Dashboard | AgriPredict Input Suppliers' />
</svelte:head>

<section class='container mx-auto max-w-[60rem]  font-sans'>
	<div class='grid grid-cols-3 gap-5'>
		<div class='col-span-2 space-y-3.5'>
			<div class='bg-white rounded-lg p-4 shadow-md'>
				<h1 class='text-md font-extrabold'>News</h1>
				<h2 class='text-sm text-gray-500'>News will appear here along with notifications, including, announcements and system updates.</h2>
				<p class='text-sm mt-4 font-light text-md'>Turn on browser notifications so you don&apos;t miss any updates.&nbsp;<a class='text-blue-500' href='/dashboard'>Learn More</a></p>
			</div>
			<div class='bg-white rounded-lg p-4 shadow-md'>
				<h1 class='text-md font-extrabold'>Pending Listings</h1>
				<h2 class='text-sm text-gray-500'>All listing the require manual review.</h2>
			</div>
		</div>
		<div class='space-y-3.5'>
			<div class='bg-white rounded-lg p-4 shadow-md flex flex-col'>
				<div class='flex flex-col'>
					<h1 class='text-md font-extrabold'>Transactions Summary</h1>
					<h2 class='text-sm text-gray-500'>Last 7 days</h2>
				</div>
				<div class='my-3 space-y-1.5'>
					<div class='flex justify-between w-full'>
						<div class='text-sm text-gray-600'>New Listings</div>
						<div class='text-sm font-semibold text-end text-gray-900'>0</div>
					</div>
					<div class='flex justify-between w-full'>
						<div class='text-sm text-gray-600'>Matches</div>
						<div class='text-sm font-semibold text-end text-gray-900'>0</div>
					</div>
					<div class='flex justify-between w-full'>
						<div class='text-sm text-gray-600'>Offers</div>
						<div class='text-sm font-semibold text-end text-gray-900'>0</div>
					</div>
				</div>
				<a href='/dashboard/reports' class='py-1.5 px-5 text-md bg-gray-50 text-center text-gray-900 focus:outline-none rounded-md border border-gray-200 hover:bg-gray-100 hover:text-gray-900 focus:z-10 focus:ring-4 focus:ring-gray-200'>View Report</a>
			</div>
			<div class='bg-white rounded-lg p-4 shadow-md'>
				<h1 class='text-md font-extrabold'>Messaging</h1>
			</div>
		</div>
	</div>
</section>
