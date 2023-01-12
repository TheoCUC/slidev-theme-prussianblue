<script>
export default {
  props: {
    layout: {
      type: String,
      required: false,
      default: 'center'
    },
    url: {
      type: String,
      required: false,
      default: 'https://cn.sli.dev/logo.svg'
    },
    h: {
      type: String,
      required: false,
    }
  },
  setup(props) {
    let imageheight = ""
    // 判断是否输入了h值
    if (props.h) {
      // 如果输入了h值，就把h值赋值给imagepos
      imageheight = `h-${props.h} `;
      // return { imagepos };
      // console.log(props.h)
    }
    let imagepos = "";
    if (props.layout == "right" || props.layout == "r") {
      // 向右浮动
      imagepos = "float-right";
    } else if (props.layout == "center" || props.layout == "c") {
      // 居中
      imagepos = "mx-auto";
    } else if (props.layout == "rt") {
      // 右上方悬停
      imagepos = "absolute top-10 right-10 -z-1";
    }
    imagepos = imageheight + imagepos
    // console.log("imagepos:", imagepos)
    return { imagepos };
  },
  methods: {
    show() {
      window.open(this.url);
    }
  }
}
</script>

<template>
  <img :src="url" :href="url" alt="image" :class="imagepos" class="shadow-md cursor-pointer rounded-xl border-image"
    @click="show" />
</template>s