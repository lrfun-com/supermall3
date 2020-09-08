<template>
  <div class="remmends">
    <div class="remmends-item" v-for="item in recommends">
      <a :href="item.link">
        <img :src="item.image" alt="">
        <div>{{item.title}}</div>
      </a>
    </div>
  </div>
</template>

<script>
  export default {
    name: "RemmendsView",
    props: {
      recommends: {
        type: Array,
        default: []
      }
    }
  }
</script>

<style scoped>
  .remmends{
    display: flex;
    padding: 10px 0 20px;
    border-bottom: 8px solid #eeeeee;
  }
  .remmends-item {
    flex: 1;
    text-align: center;
    font-size: 12px;
  }
  .remmends-item img {
    width: 90%;
    margin-bottom: 5px;
  }
</style>
