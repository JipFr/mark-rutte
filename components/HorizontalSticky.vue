<template>
  <article
    ref="main"
    class="horizontal-sticky"
    :style="`top: ${y}px; left: ${x}px; background-position: -${bg.x}px -${bg.y}px; transform: rotate(${rotation}deg); z-index: ${zIndex};`"
  >
    <div class="padding draggable"></div>
    <div class="sticky-content">
      <slot />
    </div>
  </article>
</template>

<style lang="scss" scoped>
.horizontal-sticky {
  background-image: url(/stickies.png);
  background-size: 1000px;
  width: 190px;
  height: 50px;
  display: flex;
  position: absolute;
}
.padding {
  width: 35px;
  height: 45px;
  margin-right: 10px;
}
.draggable {
  cursor: pointer;
}
</style>

<script>
const uvMaps = []
const marginX = 1
const marginY = 5

for (let i = 0; i < 9; i++) {
  uvMaps.push({
    x: marginX,
    y: marginY + 60 * i,
  })
  uvMaps.push({
    x: marginX + 210,
    y: marginY + 60 * i,
  })
}

export default {
  data() {
    return {
      x: 0,
      y: 0,
      mouseDown: false,
      rotation: Math.random() * 30 - 15,
      bg: uvMaps[Math.floor(Math.random() * uvMaps.length)],
      zIndex: Math.floor(Date.now() / 1e3),
    }
  },
  mounted() {
    const self = this.$refs.main
    const parentNode = this.$refs.main.parentNode.parentNode

    this.x = Math.floor(
      Math.random() * (parentNode.scrollWidth - self.scrollWidth)
    )
    this.y = Math.floor(
      Math.random() * (parentNode.scrollHeight - self.scrollHeight)
    )

    document.addEventListener('mousemove', this.onMouseMove)

    self
      .querySelector('.draggable')
      .addEventListener('mousedown', this.onMouseDown)

    document.addEventListener('mouseup', this.onMouseUp)
  },
  methods: {
    onMouseMove(evt) {
      if (this.mouseDown) {
        this.x += evt.movementX
        this.y += evt.movementY
      }
    },
    onMouseDown() {
      this.mouseDown = true
      this.zIndex = Math.floor(Date.now() / 1e3)
    },
    onMouseUp() {
      this.mouseDown = false
    },
  },
}
</script>
