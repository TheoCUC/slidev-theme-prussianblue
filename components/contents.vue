<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  props: {
    id: {
      type: Number,
      required: true,
    },
    contentsValue: {
      type: String,
      required: true,
    },
  },
  setup(props) {
			const input = props.contentsValue;
			var output = "";
			var texts = input.split("|");
			var color = "text-blue-gray-500";
			for (let i = 0; i < texts.length; i++) {
				if (i == props.id - 1) {
					color = "text-white";
        }
        output += '<div class="flex-auto ' + color + ' text-center px-5">' + texts[i] + "</div>";
        color = "text-blue-gray-500";
			}
			const message = output;
			return { message };
  },
})
</script>

<template>
  <div class="z-90 flex absolute bottom-0 w-full py-8px">
    <span v-html="message" class="flex w-full"></span>
  </div>
</template>