<template>
  <div class="GoodsListItem">
    <img
      :src="goodsItem.show.img"
      alt=""
    >
    <div class="goods-info">
      <p>{{goodsItem.title}}</p>
      <span class="price">{{goodsItem.price}}</span>
      <span class="collection">{{goodsItem.cfav}}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'GoodsListItem',
  props: {
    goodsItem: {
      type: Object,
      default () {
        return {}
      }
    }
  }
}
</script>

<style>
.GoodsListItem {
    position: relative;
    padding-bottom: 40px;
    width: 48%;
}
.GoodsListItem img {
  width: 100%;
  border-radius: 5px;
}
.goods-info {
    font-size: 12px;
    position: absolute;
    bottom: 7px;
    left: 0;
    right: 0;
    overflow: hidden;
    text-align: center;
}
.goods-info p {
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
    margin-bottom: 3px;
    color: slategray;
    font-size: 14px;
}
.goods-info .price{
    margin-right: 40px;
    position: relative;
    color: #db639b;
}
.goods-info .price::before{
    content: '';
    position: absolute;
    left: -18px;
    top: 2px;
    width: 14px;
    height: 14px;
    background: url("../../../assets/img/goods/价格.svg") 0 0/14px 14px;
}
.goods-info .collection{
    position: relative;
}
.goods-info .collection::before{
    content: '';
    position: absolute;
    left: -15px;
    top: 2px;
    width: 14px;
    height: 14px;
    background: url("../../../assets/img/goods/收藏.svg") 0 0/14px 14px;
}
</style>