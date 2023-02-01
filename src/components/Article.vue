<template>
  <div class="article">
    <div class="article__left">
      <div class="article__title">我是文章名</div>
      <div class="article__desc">这是这篇文章的描述，如果你想了解具体内容请点击进去这是这篇文章的描述，如果你想了解具体内容请点击进去</div>
      <ul class="article__info">
        <li class="article__fields">
          <div class="article__icon i-carbon-view"></div>
          <span>200</span>
        </li>
        <li class="article__fields">
          <div class="article__icon i-carbon-thumbs-up"></div>
          <span>200</span>
        </li>
        <li class="article__fields">
          <div class="article__icon i-carbon-favorite"></div>
          <span>200</span>
        </li>
      </ul>
    </div>
    <img class="article__image" src="https://img2.baidu.com/it/u=3352691132,3791525957&fm=253&fmt=auto&app=120&f=JPEG?w=800&h=500" />
  </div>
</template>
<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  setup() {
    
  },
})
</script>

<style lang="scss" scoped>
.article {
  display: flex;
  min-width: 0;
  padding: 20px;
  &__left {
    flex: 1;
    min-width: 0; //重点样式
  }
  &__title {
    margin-bottom: 10px;
    font-size: 18px;
    font-weight: bold;
    color: #1d2129;
  }
  &__desc {
    margin-bottom: 10px;
    font-size: 14px;
    color: #86909c;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  &__info {
    display: flex;
    color: var(--text-light);
    .article__fields {
      display: flex;
      align-items: center;
      margin-right: 20px;
    }
    .article__icon {
      margin-right: 10px;
    }
  }
  &__image {
    flex-shrink: 0;
    width: 125px;
    height: 100px;
    margin-left: 20px;
    border: 1px solid #000;
    object-fit: cover;
  }
}
</style>
