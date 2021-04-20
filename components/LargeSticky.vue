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
  width: 210px;
  height: 215px;
  position: absolute;
}
.padding {
  width: 100%;
  height: 45px;
}
.draggable {
  cursor: pointer;
}
.sticky-content {
  margin: 10px 20px;
}
</style>

<script>
const marginX = 1
const marginY = 540
// const uvMaps = [{ x: marginX, y: marginY }]
const uvMaps = []

for (let i = 0; i < 4; i++) {
  uvMaps.push({
    x: marginX + 235 * i,
    y: marginY,
  })
  uvMaps.push({
    x: marginX + 235 * i,
    y: marginY + 240,
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
