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
		<div
			class="-z-2 bg-white shadow-lg rounded-md flex absolute mx-auto my-10 w-9/10 h-85/100 left-12 top-0"
		>
			<div class="slidev-layout default">
				<div class="my-auto">
					<slot />
				</div>
			</div>
		</div>

		<div class="-z-1 flex absolute bottom-0 w-full py-8px">
			<contents :id="id" :contentsValue="$slidev.configs.contents"></contents>
		</div>
		<div class="bg-pblue -z-3 flex absolute w-full h-1/3 left-0 bottom-0"></div>
		<div
			class="bg-pblue -z-1 shadow-lg rounded-md flex absolute w-1/5 h-1/25 mx-98 my-8 top-0"
		></div>
	</div>
</template>
