<template>
	<div>
		<div class="bg-white z-1 shadow-lg rounded-md flex absolute mx-auto my-10 w-9/10 h-85/100 left-12 top-0">
			<div class="slidev-layout cover flex items-center">
				<div class="my-auto my-3  object-center">
					<slot />
				</div>
			</div>
		</div>
		<div class="bg-[#002c47] flex absolute w-full h-1/3 left-0 bottom-0"></div>
		<div class="bg-[#002c47] z-2 rounded-md flex absolute w-1/5 h-1/25 left-0 right-0 top-8 mx-auto"></div>
	</div>
</template>
