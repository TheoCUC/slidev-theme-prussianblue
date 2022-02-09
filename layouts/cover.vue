<template>
	<div>
		<div class="z-20 bg-white z-20 shadow-lg rounded-md flex absolute mx-auto my-10 w-9/10 h-85/100 left-12 top-0">
		<div class="slidev-layout cover">
			<div class="my-auto my-100px object-center">
				<slot />
			</div>
		</div>
		</div>
		<div class="bg-pblue z-10 flex absolute w-full h-1/3 left-0 bottom-0"></div>
		<div class="bg-pblue z-30 shadow-lg rounded-md flex absolute w-1/5 h-1/25 mx-98 my-8 top-0"></div>
	</div>
</template>