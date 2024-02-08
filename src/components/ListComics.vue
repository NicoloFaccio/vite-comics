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
        <div>
          <a :href="propsThumb"></a>
          <span>{{ propsSeries }}</span>
        </div>
    </div>
</template>

<style scoped lang="scss">
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;
</style>