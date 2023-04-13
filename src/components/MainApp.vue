<script>
export default {
  name: "MainApp",
  data() {
    return {};
  },
};
</script>

<template>
  <section class="main-top">
    <div class="card-container">
      <div class="card">
        <img src="../assets/img/buy-comics-digital-comics.png" alt="" />
        <p>DIGITAL COMICS</p>
      </div>
      <div class="card">
        <img src="../assets/img/buy-comics-merchandise.png" alt="" />
        <p>MERCHANDISE</p>
      </div>
      <div class="card">
        <img src="../assets/img/buy-comics-shop-locator.png" alt="" />
        <p>SHOP LOCATOR</p>
      </div>
      <div class="card">
        <img src="../assets/img/buy-comics-subscriptions.png" alt="" />
        <p>SUBSCRIPTION</p>
      </div>
      <div class="card">
        <img src="../assets/img/buy-dc-power-visa.svg" alt="" />
        <p>DC POWER VISA</p>
      </div>
    </div>
  </section>
  <section class="main-bottom">
    <div class="main-bottom-list">
      <div class="left-list">
        <h3>DC COMICS</h3>
        <ul>
          <li>Characters</li>
          <li>Comics</li>
          <li>Movies</li>
          <li>Tv</li>
          <li>Games</li>
          <li>Videos</li>
          <li>News</li>
        </ul>

        <h3>SHOP</h3>
        <ul>
          <li>shop DC</li>
          <li>shop DC collectibles</li>
        </ul>
      </div>
      <div class="center-list">
        <h3>DC</h3>
        <ul>
            <li>Terms of use</li>
            <li>Privacy policy(new)</li>
            <li>Ad choice</li>
            <li>Advertaising</li>
            <li>Jobs</li>
            <li>Subscriptions</li>
            <li>Talent workshops</li>
            <li>CPSC Certificate</li>
            <li>Ratings</li>
            <li>Shop help</li>
            <li>Contact use</li>
        </ul>
      </div>
      <div class="rigth-list">
        <h3>SITES</h3>
        <ul>
            <li>DC</li>
            <li>MAD magazine</li>
            <li>DC kids</li>
            <li>DC Universe</li>
            <li>DC Power visa</li>
        </ul>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variabals" as *;

.main-top {
  height: 140px;
  background-color: $main-color;

  .card-container {
    width: 70%;
    height: 100%;
    margin: 0 auto;

    @include flex(row, start, center);

    .card {
      @include flex(row, start, center);
      color: $color-title;
      margin: 0 1.5rem;

      img {
        width: 40px;
      }

      p {
        margin: 0 0.6rem;
        font-size: 0.8rem;
      }
    }
  }
}

.main-bottom {
  height: 300px;
  background-image: url("../assets/img/footer-bg.jpg");

  .main-bottom-list {
    width: 70%;
    height: 100%;
    margin: 0 auto;
    padding-top: 30px;

    @include flex (row, start, start);

    h3 {
        color: $color-title;
    }

    li {
        list-style: none;
        color: $color-title;
        font-weight: 200;
        font-size: .6rem;
        margin: .6rem 0;
    }

    .center-list {
        margin: 0 2rem;
    }

  }
}
</style>
