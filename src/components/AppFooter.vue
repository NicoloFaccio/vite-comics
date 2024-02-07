<script>
  export default{
    name: "AppFooter",

    data(){
        return{
            ArrayFirstList: [
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
                    name: "TV",
                    link: "#"
                },
                {
                    name: "games",
                    link: "#"
                },
                {
                    name: "videos",
                    link: "#"
                },
                {
                    name: "news",
                    link: "#"
                }
            ],

            ArraySecondtList: [
                {
                    name: "shop DC",
                    link: "#"
                },
                {
                    name: "shop DC collectibles",
                    link: "#"
                }
            ],

            ArrayThirdtList: [
                {
                    name: "therms of use",
                    link: "#"
                },
                {
                    name: "privacy policy (new)",
                    link: "#"
                },
                {
                    name: "ad choises",
                    link: "#"
                },
                {
                    name: "advertising",
                    link: "#"
                },
                {
                    name: "jobs",
                    link: "#"
                },
                {
                    name: "subscriptons",
                    link: "#"
                },
                {
                    name: "talent workshop",
                    link: "#"
                },
                {
                    name: "CPSC certificates",
                    link: "#"
                },
                {
                    name: "ratings",
                    link: "#"
                },
                {
                    name: "shop help",
                    link: "#"
                },
                {
                    name: "contact us",
                    link: "#"
                }
            ],

            ArrayFourthtList: [
                {
                    name: "DC",
                    link: "#"
                },
                {
                    name: "MAD magazine",
                    link: "#"
                },
                {
                    name: "DC kids",
                    link: "#"
                },
                {
                    name: "DC univers",
                    link: "#"
                },
                {
                    name: "DC power visa",
                    link: "#"
                }
            ]
        }
    }
    
  }
</script>

<template>
    <footer>
        <section>
            <div>
                <div>
                    <h3>dc comics</h3>
                    <ul>
                        <li v-for="(element, index) in ArrayFirstList" :key="index">
                            <a :href="element.link">{{ element.name }}</a>
                        </li>
                    </ul>

                    <h3>shop</h3>
                    <ul>
                        <li v-for="(element, index) in ArraySecondtList" :key="index">
                            <a :href="element.link">{{ element.name }}</a>
                        </li>
                    </ul>
                </div>

                <div>
                    <h3>dc</h3>
                    <ul>
                        <li v-for="(element, index) in ArrayThirdtList" :key="index">
                            <a :href="element.link">{{ element.name }}</a>
                        </li>
                    </ul>
                </div>

                <div>
                    <h3>sites</h3>
                    <ul>
                        <li v-for="(element, index) in ArrayFourthtList" :key="index">
                            <a :href="element.link">{{ element.name }}</a>
                        </li>
                    </ul>
                </div>
            </div>
        </section>

        <section>

        </section>
    </footer>
</template>

<style scoped lang="scss">
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

section:first-child{
    > div {
        margin: 0 auto;
        width: 70%;
        padding: 30px 0;

        display: flex;
        gap: 25px;
        div {
            h3 {
                color: white;
                text-transform: $textUppercase;
                padding-block: 10px;
            }

            ul {
                line-height: 180%;
                li{
                    a{
                        color: rgba(119, 124, 120, 1);
                        text-transform: $textCapitalize;
                    }
                }
            } 
        }
    }

    background-image: url("../assets/img/footer-bg.jpg");
    @include BackgroundImage
}
</style>


