<script>
  export default{
    name: "ListComics",
    props: {
      propsThumb: String,
      propsSeries: String
    }
  }
</script>

<template>
  <div>
    <figure>
      <img :src="`${propsThumb}`" alt="comics pictures">
    </figure>
    <h4>{{ propsSeries }}</h4>
  </div>
</template>

<style scoped lang="scss">
  @use '../styles/partials/variables' as *;
  @use '../styles/partials/mixins' as *;

  div{
    width: calc(100% / 6 - 30px);

    padding-top: 30px;
    display: flex;
    flex-direction: column;
    align-items: center;

    figure{
      img{
        width: 100%;
        display: block;
      }
    }

    h4 {
      text-transform: $textUppercase;
      font-weight: bold;
      margin-top: 10px;
    }
  }
</style>