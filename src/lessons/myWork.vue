<template>
  <div class="mingjing">
    <h1 class="header">JOSIE'S WORK OF ART</h1>
    <ul class="header2">
      <li class="m1">UIUX</li>
      <li class="m1">GRAPHIC DESIGN</li>
      <li class="m1">METAL CRAFT/JEWELRY DESIGN</li>
      <li class="m1">ABOUT</li>
      <li class="m1">CONTACT</li>
    </ul>
    <div class="minjing__imageGroup">
      <img class="mingjing__iphone" src="@/assets/iPhone XS Copy 5.jpg" />
      <img class="mingjing__iphone" src="@/assets/d.png" />
    </div>
  </div>
</template>
<style lang="scss" scoped>
.mingjing {
  background-color: white;
  text-align: center;
}
.header {
  font-size: 24px;
}
.header2 {
  display: flex;
  list-style: none;
  background-color: black;
  justify-content: center;
  .m1 {
    margin: 20px;
    color: white;
  }
}
.minjing__imageGroup {
  padding-top: 150px;
}
.mingjing__iphone {
  width: 400px;
  margin: auto;
  margin-top: 10px;
  // margin:150px;
}
</style>
