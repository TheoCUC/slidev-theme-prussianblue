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
	<div>
		<div class="z-1 bg-white shadow-lg rounded-md flex absolute mx-auto my-10 w-9/10 h-85/100 left-12 top-0">
			<div class="slidev-layout default w-full pt-6">
				<div class="my-auto">
					<slot />
				</div>
			</div>
		</div>

		<div class="flex absolute bottom-0 w-full py-8px">
			<contents :id="id" :contentsValue="$slidev.configs.contents"></contents>
		</div>
		<div class="bg-[#002c47] flex absolute w-full h-1/3 left-0 bottom-0"></div>
		<div class="bg-[#002c47] z-2 rounded-md flex absolute w-1/5 h-1/25 left-0 right-0 top-8 mx-auto"></div>
	</div>
</template>
