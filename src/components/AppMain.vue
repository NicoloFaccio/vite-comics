<script>
  import ListComics from "./ListComics.vue"

  export default{
    name: "AppMain",

    components: {
      ListComics
    },

    data(){
      return {
        ArrayIcons: [
          {
            name: "digital comics",
            link: "#",
            image:"./src/assets/img/buy-comics-digital-comics.png"
          },
          {
            name: "dc merchandise",
            link: "#",
            image:"./src/assets/img/buy-comics-merchandise.png"
          },
          {
            name: "subscriptions",
            link: "#",
            image:"./src/assets/img/buy-comics-subscriptions.png"
          },
          {
            name: "comic shop locator",
            link: "#",
            image:"./src/assets/img/buy-comics-shop-locator.png"
          },
          {
            name: "dc power visa",
            link: "#",
            image:"./src/assets/img/buy-dc-power-visa.svg"
          }
        ],

        ArrayComics: [
          {
            "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
            "price": "$19.99",
            "series": "Action Comics",
            "type": "comic book"
          },
          {
            "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
            "price": "$3.99",
            "series": "American Vampire 1976",
            "type": "comic book"
          },
          {
            "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
            "price": "$16.99",
            "series": "Aquaman",
            "type": "graphic novel"
          },
          {
            "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
            "price": "$2.99",
            "series": "Batgirl",
            "type": "comic book"
          },
          {
            "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
            "price": "$3.99",
            "series": "Batman",
            "type": "comic book"
          },
          {
            "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
            "price": "$2.99",
            "series": "Batman Beyond",
            "type": "comic book"
          },
          {
            "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
            "price": "$3.99",
            "series": "Batman/Superman",
            "type": "comic book"
          },
          {
            "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
            "price": "$4.99",
            "series": "Batman/Superman Annual",
            "type": "comic book"
          },
          {
            "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
            "price": "$5.99",
            "series": "Batman: The Joker War Zone",
            "type": "comic book"
          },
          {
            "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
            "price": "$6.99",
            "series": "Batman: Three Jokers",
            "type": "comic book"
          },
          {
            "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
            "price": "$4.99",
            "series": "Batman: White Knight Presents: Harley Quinn",
            "type": "comic book"
          },
          {
            "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
            "price": "$16.99",
            "series": "Catwoman",
            "type": "graphic novel"
          }
        ]
      }
    }
  }
</script>

<template>
  <main>
    <section>
      <div class="jumbotron">

      </div>

      <div class="comics">
        <h2>current series</h2>
        <ListComics 
      v-for="(element, index) in ArrayComics" 
      :key="index"
      :propsThumb="element.thumb"
      :propsSeries="element.series"
      />
      </div>

      <div class="button-load">
        <button>
          load more
        </button>
      </div>
    </section>

    <section>
      <div>
        <figure v-for="(element, index) in ArrayIcons" :key="index" >
          <img width="40px" :src="`${element.image}`" alt="Icons">
          <span>
            <a height="50px" :href="element.link">
              {{ element.name }}
            </a> 
          </span>
        </figure>
      </div>
    </section>
  </main>
</template>

<style scoped lang="scss">
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

  main{
    section:first-child  {
      background-color: rgba(28, 28, 28, 1);

      .jumbotron {
        background-image: url("../assets/img/jumbotron.jpg");
        background-repeat: no-repeat;
        background-position: top;
        background-size: cover;
        min-height: 400px;
      }

      .comics {
        @include GeneralWidth;

        color: white;

        padding: 40px 0;

        display: flex;
        flex-wrap: wrap;
        gap: 30px;
        position: relative;

        h2 {
          position: absolute;
          top: -25px;

          background-color: $ColorBlue;
          color: white;
          font-weight: bold;
          text-transform: $textUppercase;
          padding: 10px;
        }
      }

      .button-load {
        display: flex;
        justify-content: center;
        padding-block: 30px;

        button {
          background-color: $ColorBlue;
          padding: 10px 20px;
          border: none;
          color: white;
          text-transform: $textUppercase;
          font-weight: bold;
        }
      }
    }

    section:last-child  {
      background-color: $ColorBlue;

      div{
        @include GeneralWidth;
        color: white;
        padding: 40px 0;

        @include PositionFlex;

        figure{
          display: flex;
          align-items: center;
          gap: 10px;
          span{
            text-transform: uppercase;
            a {
              color: white;
            }
          }
        }
      }
    }
  }
</style>
