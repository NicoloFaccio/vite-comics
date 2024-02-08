<script>
  export default{
    name: "AppMain",

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
        ]
      }
    }
  }
</script>

<template>
  <main>
    <section>
      <div>
        --Content goes here--
      </div>
    </section>

    <section>
      <div>
        <figure v-for="(element, index) in ArrayIcons" :key="index" >
          <img width="40px" :src="`${element.image}`" alt="Icons">
          <span>
            <a :href="element.link">
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

      div{
        @include GeneralWidth;

        color: white;

        padding: 40px 0;
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
