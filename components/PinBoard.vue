<template>
  <div class="pinboard-container">
    <div class="pinboard">
      <div class="ratio"></div>
      <div class="content-wrapper">
        <div class="content">
          <HorizontalSticky> Hallos </HorizontalSticky>
          <!-- <HorizontalSticky> LOL! </HorizontalSticky>
          <HorizontalSticky> XD </HorizontalSticky>
          <HorizontalSticky> Lol </HorizontalSticky>
          <HorizontalSticky> Lol </HorizontalSticky>
          <HorizontalSticky> Lol </HorizontalSticky>
          <HorizontalSticky> Lol </HorizontalSticky>
          <HorizontalSticky> Lol </HorizontalSticky>
          <HorizontalSticky> Lol </HorizontalSticky>
          <HorizontalSticky> Lol </HorizontalSticky>
          <HorizontalSticky> Lol </HorizontalSticky>
          <HorizontalSticky> Lol </HorizontalSticky>
          <HorizontalSticky> Lol </HorizontalSticky> -->
          <HorizontalSticky> Lol </HorizontalSticky>
          <HorizontalSticky> Lol </HorizontalSticky>
          <HorizontalSticky> Lol </HorizontalSticky>
          <HorizontalSticky> Lol </HorizontalSticky>
          <HorizontalSticky> Lol </HorizontalSticky>
          <LargeSticky>HELLO!</LargeSticky>
          <LargeSticky>HELLO!</LargeSticky>
          <LargeSticky>HELLO!</LargeSticky>
          <LargeSticky>HELLO!</LargeSticky>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.pinboard-container {
  background: url(http://2.bp.blogspot.com/-HPWq5_H10Bs/U4NbaH3_WoI/AAAAAAAAO-w/3tOklJ2MBcE/w1200-h630-p-k-no-nu/Seamless_Natural_Wood_Texture.jpg);
  padding: 10px;
  user-select: none;
}
.pinboard {
  width: 100%;
  background: url(https://st.depositphotos.com/1032753/4936/i/950/depositphotos_49366379-stock-photo-seamless-pinboard-texture.jpg);
  position: relative;
  overflow: hidden;

  .ratio {
    padding-bottom: 100%;
  }
  .content-wrapper {
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;

    .content {
      position: relative;
    }
  }
}
</style>
