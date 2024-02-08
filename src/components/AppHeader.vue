<script>
  export default{
    name: "AppHeader",
    data(){
        return {
            ArrayNav: [
                {
                    name: "characters",
                    link: "#"
                },
                {
                    name: "comics",
                    link: "#"
                },
                {
                    name: "movies",
                    link: "#"
                },
                {
                    name: "tv",
                    link: "#"
                },
                {
                    name: "games",
                    link: "#"
                },
                {
                    name: "collectibles",
                    link: "#"
                },
                {
                    name: "videos",
                    link: "#"
                },
                {
                    name: "fans",
                    link: "#"
                },
                {
                    name: "news",
                    link: "#"
                },
                {
                    name: "shop",
                    link: "#"
                },
            ]
        }
    }
  }
</script>

<template>
    <header>
        <div>
            <figure>
                <img width="80px" src="../assets/img/dc-logo.png" alt="logo">
            </figure>

            <nav>
                <ul>
                    <li v-for="(element, index) in ArrayNav" :key="index">
                       <a :href="element.link">{{ element.name }}</a>
                    </li>
                </ul>
            </nav>
            
        </div>
    </header>
</template>

<style scoped lang="scss">
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

    header{
        > div {
            @include PositionFlex;

            @include GeneralWidth;

            text-transform: uppercase;

            figure{
                padding: 20px 0;
            }
            
            nav {
                ul {
                    display: flex;
                    gap: 15px;

                    li {
                        &:hover{ 
                            border-bottom: 1px solid $ColorBlue;
                        }

                        a {
                            color: rgba(104, 92, 86, 1);
                            font-weight: bold;
                            &:hover{ 
                                color: $ColorBlue;
                            }
                        }
                    }
                }
            }
        }
    }
</style>


