<script>
import { defineComponent } from "vue";

export default defineComponent({
	props: {
		id: {
			type: Number,
			required: true,
		},
	},
});
</script>
<template>
	<div class="relative h-full">
		<div class="z-20 bg-white shadow-lg rounded-md flex absolute mx-auto my-10 w-9/10 h-85/100 left-12 top-0">
			<div class="slidev-layout default w-full pt-6">
				<div class="my-auto">
					<slot />
				</div>
			</div>
		</div>

		<div class="flex absolute bottom-0 w-full py-8px">
			<contents :id="id" :contentsValue="$slidev.configs.contents"></contents>
		</div>
		<div class="bg-[#002c47] absolute z-10 w-full h-48 left-0 right-0 bottom-0 mx-auto"> </div>
		<div class="bg-[#002c47] absolute z-30 rounded-md w-48 h-6 left-0 right-0 top-8 mx-auto"> </div>
	</div>
</template>
