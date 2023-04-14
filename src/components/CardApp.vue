<script>
export default {
  name: "CardApp",
  props: {
    img: String,
    series: String,
  },
};
</script>

<template>
    <div class="card">
      <img :src="img" alt="" />
      <h3>{{ series }}</h3>
    </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variabals" as *;

.card {
  width: calc(100% / 6 - 20px);
  margin: 10px;

  h3 {
    font-size: .8rem;
    color: $color-title;
  }

  img {
    width: 150px;
    height: 170px;
    object-fit: cover;
  }
}
</style>
