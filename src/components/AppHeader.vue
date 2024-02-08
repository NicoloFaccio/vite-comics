<script>
  export default{
    name: "AppHeader",

    data(){
        return {
            ArrayNav: [
                {
                    name: "characters",
                    link: "#",
                    current: false
                },
                {
                    name: "comics",
                    link: "#",
                    current: true
                },
                {
                    name: "movies",
                    link: "#",
                    current: false
                },
                {
                    name: "tv",
                    link: "#",
                    current: false
                },
                {
                    name: "games",
                    link: "#",
                    current: false
                },
                {
                    name: "collectibles",
                    link: "#",
                    current: false
                },
                {
                    name: "videos",
                    link: "#",
                    current: false
                },
                {
                    name: "fans",
                    link: "#",
                    current: false
                },
                {
                    name: "news",
                    link: "#",
                    current: false
                },
                {
                    name: "shop",
                    link: "#",
                    current: false
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
                    <li 
                      v-for="(element, index) in ArrayNav" 
                      :key="index"
                      :class="element.current ? 'active-bottom' : ''">
                        <a
                        :class="element.current ? 'active' : ''"
                          :href="element.link">
                            {{ element.name }}
                        </a>
                    </li>
                </ul>
            </nav>
            
        </div>
    </header>
</template>

<style scoped lang="scss">
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

.active-bottom{
    border-bottom: 3px solid $ColorBlue;
}
.active {
    color: $ColorBlue;
}

    header{
        > div {
            @include PositionFlex;

            @include GeneralWidth;

            text-transform: uppercase;

            height: 130px;

            figure{
                padding: 20px 0;
            }
            
            nav {
                ul {
                    display: flex;
                    gap: 15px;

                    li {
                        line-height: 125px;

                        a {
                            color: rgba(104, 92, 86, 1);
                            font-weight: bold;

                            &:hover {
                                color: $ColorBlue;
                            }

                        }
                    }
                }
            }
        }
    }
</style>


