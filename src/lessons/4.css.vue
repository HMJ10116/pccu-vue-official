<template>
  <div class="container pt-5 pb-5">
    <h1>白話文CSS</h1>
    <p>CSS主要有三大功能</p>
    <ol>
      <li>排列</li>
      <li>間距調整</li>
      <li>美化</li>
    </ol>
    <h2>排列</h2>
    <p>瀏覽器渲染的順序是從左到右, 從上到下, 但如果要呈現不同的排列方式或是在RWD時做出變化,</p>
    <p>就需要配合div標籤與各種css屬性來呈現不同的排列</p>
    <p>當前主流控制排列方式的方法有兩種</p>
    <ul>
      <li>Flex box: 用來控制相對位置, 呈現方式會根據欄位數量或是螢幕寬度改變</li>
      <li>Position: 用來控制絕對位置, 比如定在瀏覽器的最上方, 或是某個容器內的右上角</li>
    </ul>
    <h3>Flex box</h3>
    <p>普通排列</p>
    <myCard>
      <div>
        <span class="border text-primary">普通排列</span>
        <span class="border text-primary">普通排列</span>
        <span class="border text-primary">普通排列</span>
      </div>
    </myCard>
    <p>在調整css之後, 改為垂直排列</p>
    <myCard>
      <div class="d-flex flex-column">
        <span class="border text-primary">垂直排列</span>
        <span class="border text-primary">垂直排列</span>
        <span class="border text-primary">垂直排列</span>
      </div>
    </myCard>
    <p>在調整css之後, 改為均勻分布</p>
    <myCard>
      <div class="d-flex justify-content-between">
        <span class="border text-primary">均分空間</span>
        <span class="border text-primary">均分空間</span>
        <span class="border text-primary">均分空間</span>
      </div>
    </myCard>
    <p>在調整css之後, 改為置中</p>
    <myCard>
      <div class="d-flex justify-content-center">
        <span class="border text-primary">靠中</span>
        <span class="border text-primary">靠中</span>
        <span class="border text-primary">靠中</span>
      </div>
    </myCard>
    <p>在調整css之後, 改為置末</p>
    <myCard>
      <div class="d-flex justify-content-end">
        <span class="border text-primary">靠尾</span>
        <span class="border text-primary">靠尾</span>
        <span class="border text-primary">靠尾</span>
      </div>
    </myCard>
    <p>還有align-self: center可以使標籤自我置中, 但比較進階可以之後再來研究</p>
    <h3>Position</h3>
    <p>在調整css之前</p>
    <myCard>
      <span class="border text-primary">普通排列</span>
      <span class="border text-primary">普通排列</span>
      <span class="border text-primary">普通排列</span>
      <span class="border text-primary">還沒固定右上角</span>
    </myCard>
    <p>在調整css之後</p>
    <myCard class="position-relative">
      <span class="border text-primary">普通排列</span>
      <span class="border text-primary">普通排列</span>
      <span class="border text-primary">普通排列</span>
      <span class="border text-primary fixed-top-right">現在固定右上角</span>
    </myCard>
    <h2>間距調整</h2>
    <p>首先要了解網頁佈局中的兩的概念，容器與內容。</p>
    <p>網頁中容器與內容的關係，就像俄羅斯娃哇一樣，雞生蛋蛋生雞，一個容器可以是其他容器的內容，一個內容可以是其他容器的容器。</p>
    <ul>
      <li>Margin: 控制容器間的距離</li>
      <li>Padding: 控制容器與內容的距離</li>
    </ul>
    <h3>Margin</h3>
    <div class="d-flex">
      <myCard>
        <span>沒有間距</span>
      </myCard>
      <myCard>
        <span>沒有間距</span>
      </myCard>
    </div>
    <div class="d-flex">
      <myCard class="mr-3">
        <span>有間距</span>
      </myCard>
      <myCard>
        <span>有間距</span>
      </myCard>
    </div>
    <h3>Padding</h3>
    <div class="d-flex">
      <myCard>
        <span>沒有間距</span>
      </myCard>
      <myCard>
        <span>沒有間距</span>
      </myCard>
    </div>
    <div class="d-flex">
      <myCard>
        <div class="p-3">
          <span>有間距</span>
        </div>
      </myCard>
      <myCard>
        <div class="p-3">
          <span>有間距</span>
        </div>
      </myCard>
    </div>
    <h2>美化</h2>
    <p>美化的基礎就是控制顏色與大小，他的複雜度比單純的排列與調整間距更高</p>
    <p>以下僅列出常用的美化屬性</p>
    <span>文字相關</span>
    <ul>
      <li>color: 文字顏色</li>
      <li>font-size: 文字大小</li>
      <li>font-weight: 文字粗細</li>
      <li>line-height: 文字高度, 有時可以讓文字重直至中</li>
    </ul>
    <span>顏色</span>
    <ul>
      <li>background-color: 背景顏色</li>
    </ul>
    <span>邊框</span>
    <div class="css__border">
      <p>通常一行就解決，如border: 2px solid darkseagreen</p>
      <p>表現了邊框寬度, 邊框線條風格, 與邊框顏色</p>
    </div>
    <h2>作業</h2>
    <p>承前一題目，善用CSS屬性將你的房間與主要家具用網頁元素來呈現，表現房間的格局</p>
    <p>對於初學入門的學生，只要能以Bootstrap表示家具的相對位置即可</p>
    <p>對與有心往前端發展的學生，請挑戰自己，不使用Bootstrap來完成這次作業，並力求比例上的近似、與RWD的設計</p>
    <div class="css__demo">
      <h3 class="demo__header">範例</h3>
      <div class="demo__room">
        <span class="room__window">整面窗戶</span>
        <span class="room__tank">水草缸</span>
        <span class="room__table">桌子</span>
        <span class="room__closet">五斗米櫃</span>
        <div class="room__bed">
          床
          <div class="bed__pillowGroup">
            <span class="bed__pillow">枕頭</span>
            <span class="bed__pillow">枕頭</span>
          </div>
        </div>
        <span class="room__shelve">書櫃</span>
        <span class="entrance__door">門</span>
      </div>
    </div>
  </div>
</template>
<script>
import myCard from '@/components/myCard.vue'
export default {
  components: {
    myCard
  }
}
</script>
<style lang="scss" scoped>
.d-flex {
  display: flex;
}
.justify-content-center {
  justify-content: center;
}
.fixed-top-right {
  position: absolute;
  top: 0;
  right: 0;
}
.css__border {
  border: 2px solid darkseagreen;
}

.css__demo {
  width: 100%;
  .demo__room {
    width: 100%;
    border: 1px solid black;
    position: relative;
    width: calc(100vw - 30px);
    height: calc(70vw);
    text-align: center;
    .room__window {
      min-width: 100%;
      height: 8%;
      border: 1px solid black;
      display: block;
    }
    .room__tank {
      position: absolute;
      width: 10%;
      height: 20%;
      border: 1px solid black;
      background-color: lightgreen;
      color: white;
      left: 0;
    }
    .room__closet {
      position: absolute;
      width: 18%;
      height: 70%;
      left: 0;
      bottom: 0;
      border: 1px solid black;
    }
    .room__table {
      position: absolute;
      border: 1px solid black;
      width: 18%;
      height: 40%;
      right: 0;
    }
    .room__bed {
      position: absolute;
      left: 50%;
      bottom: 0;
      transform: translateX(-60%);
      border: 1px solid black;
      width: 40%;
      height: 60%;
      .bed__pillowGroup {
        position: absolute;
        bottom: 0;
        display: flex;
        justify-content: space-around;
        width: 100%;
        .bed__pillow {
          border: 1px solid black;
          width: 30%;
          display: block;
        }
      }
    }
    .room__shelve {
      position: absolute;
      border: 1px solid black;
      right: 0;
      top: 48%;
      width: 24%;
      height: 14%;
    }
    .entrance__door {
      position: absolute;
      border: 1px solid black;
      right: 0;
      bottom: 0;
      height: 8%;
      width: 25%;
    }
  }
}
@media (min-width: 576px) {
  .css__demo {
    .demo__room {
      max-width: 540px;
      max-height: 378px;
    }
  }
}
@media (min-width: 720px) {
  .css__demo {
    .demo__room {
      max-width: 720px;
      max-height: 500px;
    }
  }
}
@media (min-width: 992px) {
  .css__demo {
    .demo__room {
      max-width: 960px;
      max-height: 700px;
    }
  }
}
</style>
