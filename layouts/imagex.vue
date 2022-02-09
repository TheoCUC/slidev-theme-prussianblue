<script>
import { defineComponent } from 'vue'

export default defineComponent({
  props: {
    image: {
      type: String,
      required: true,
    },
    pos: {
      type: String,
      required: true,
    },
    size: {
      type: String,
      required: true,
    },
    id: {
      type: Number,
      required: true,
    },
  },
  setup(props) {
    var imagepos = "mx-auto"
    if (props.pos == "right") {
        imagepos = "float-right"
    }
    const Alignment = imagepos + ' ' + props.size
    return {Alignment}
  },
})
</script>


<template>
  <div>
    <div
      class="z-20 bg-white z-20 shadow-lg rounded-md flex absolute mx-auto my-10 w-9/10 h-85/100 left-12 top-0"
    >
      <div class="slidev-layout default">
        <div class="my-auto">
          <img :src="image" class="border-image" :class="Alignment">
          <slot />
        </div>
      </div>
    </div>

    <div class="z-90 flex absolute bottom-0 w-full py-8px">
      <contents :id="id" :contentsValue="$slidev.configs.contents"></contents>
    </div>
    <div
      class="bg-pblue z-10 flex absolute w-full h-1/3 left-0 bottom-0"
    ></div>
    <div
      class="bg-pblue z-30 shadow-lg rounded-md flex absolute w-1/5 h-1/25 mx-98 my-8 top-0"
    ></div>
  </div>
</template>