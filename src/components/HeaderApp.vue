<script>
import CardApp from "./CardApp.vue";

export default {
  name: "HeaderApp",
  components: {
    CardApp,
  },

  data() {
    return {
      links: [
        {
          text: "CHARACTERS",
          current: false,
        },
        {
          text: "COMICS",
          current: true,
        },
        {
          text: "MOVIES",
          current: false,
        },
        {
          text: "TV",
          current: false,
        },
        {
          text: "GAMES",
          current: false,
        },
        {
          text: "COLLECTIBLES",
          current: false,
        },
        {
          text: "VIDEOS",
          current: false,
        },
        {
          text: "FANS",
          current: false,
        },
        {
          text: "NEWS",
          current: false,
        },
        {
          text: "SHOP",
          current: false,
        },
      ],
      comicBooks: [
        {
          thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
          price: "$19.99",
          series: "Action Comics",
          type: "comic book",
        },
        {
          thumb:
            "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
          price: "$3.99",
          series: "American Vampire 1976",
          type: "comic book",
        },
        {
          thumb:
            "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
          price: "$16.99",
          series: "Aquaman",
          type: "graphic novel",
        },
        {
          thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
          price: "$2.99",
          series: "Batgirl",
          type: "comic book",
        },
        {
          thumb:
            "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
          price: "$3.99",
          series: "Batman",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg/revision/latest?cb=20080809201655",
          price: "$2.99",
          series: "Batman Beyond",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg/revision/latest/scale-to-width-down/1200?cb=20130627211607",
          price: "$3.99",
          series: "Batman/Superman",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg/revision/latest?cb=20200929145132",
          price: "$4.99",
          series: "Batman/Superman Annual",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg/revision/latest?cb=20200929124651",
          price: "$5.99",
          series: "Batman: The Joker War Zone",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg/revision/latest?cb=20201123054610",
          price: "$6.99",
          series: "Batman: Three Jokers",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg/revision/latest?cb=20201124094800",
          price: "$4.99",
          series: "Batman: White Knight Presents: Harley Quinn",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg/revision/latest?cb=20160303223223",
          price: "$16.99",
          series: "Catwoman",
          type: "graphic novel",
        },
      ],
    };
  },
};
</script>

<template>
  <header class="header">
    <a class="logo">
      <img src="../assets/img/dc-logo.png" alt="" />
    </a>
    <div class="header-rigth">
      <ul class="list">
        <li v-for="link in links" :class="{ active: link.current === true }">
          <a href="">
            {{ link.text }}
          </a>
        </li>
      </ul>
    </div>
  </header>

  <section class="jumbotron">
    <div class="jumbo-title">
        <h2>CURRENT SERIES</h2>
    </div>
    <div class="content">
      <CardApp
        v-for="(book, index) in comicBooks"
        :key="index"
        :img="book.thumb"
        :series="book.series"
      />
    </div>
  </section>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variabals" as *;
.header {
  width: 70%;
  height: 100px;
  margin: 0 auto;

  @include flex(row, space-between, center);

  img {
    width: 80px;
  }

  .list {
    @include flex(row, space-between, center);
  }

  li {
    list-style: none;
    margin: 0 0.4rem;
    height: 100%;

    &.active {
      border-bottom: 2px solid blue;
    }
  }

  a {
    text-decoration: none;
    font-size: 0.8rem;
    font-weight: 500;
    color: $text-color;
  }
}

.jumbotron {
  background-color: $text-color;
  
  .jumbo-title {
      width: 70%;
      margin: 0 auto;
      padding: 0 40px;
    
    h2 {
        color: $color-title;
        font-size: 1.3rem;
        background-color: $main-color;
        width: 200px;
        text-align: center;
        padding: 10px 0;
  }
  }

  .content {
    width: 70%;
    margin: 0 auto;
    padding: 40px;

    @include flex(row, center, start);
    flex-wrap: wrap;

    h3 {
      font-size: 1.5rem;
      color: $color-title;
    }
  }
}
</style>
