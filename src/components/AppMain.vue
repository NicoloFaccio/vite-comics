<script>
  export default{
    name: "AppMain"
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
        <figure>
          <img width="50px" src="../assets/img/buy-comics-digital-comics.png" alt="digital comics">
          <span>
            <a href="#">
              digital comics
            </a> 
          </span>
        </figure>

        <figure>
          <img width="50px" src="../assets/img/buy-comics-merchandise.png" alt="dc merchandise">
          <span>
            <a href="#">
              dc merchandise
            </a> 
          </span>
        </figure>

        <figure>
          <img width="50px" src="../assets/img/buy-comics-subscriptions.png" alt="subscriptions">
          <span>
            <a href="#">
              subscription
            </a> 
          </span>
        </figure>

        <figure>
          <img width="50px" src="../assets/img/buy-comics-shop-locator.png" alt="comic shop">
          <span>
            <a href="#">
              comic shop locator
            </a> 
          </span>
        </figure>

        <figure>
          <img width="50px" src="../assets/img/buy-dc-power-visa.svg" alt="dc power visa">
          <span>
            <a href="#">
              dc power visa
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
        margin: 0 auto;
        width: 70%;

        color: white;

        padding: 40px 0;
      }
    }

    section:last-child  {
      background-color: $ColorBlue;

      div{
        margin: 0 auto;
        width: 70%;
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
