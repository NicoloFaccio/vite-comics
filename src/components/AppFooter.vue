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
            ],

            ArrayContacts: [
                {
                    description: "Facebook",
                    link: "#",
                    image: "./src/assets/img/footer-facebook.png"
                },
                {
                    description: "Twitter",
                    link: "#",
                    image: "./src/assets/img/footer-twitter.png"
                },
                {
                    description: "Youtube",
                    link: "#",
                    image: "./src/assets/img/footer-youtube.png"
                },
                {
                    description: "Pinterest",
                    link: "#",
                    image: "./src/assets/img/footer-pinterest.png"
                },
                {
                    description: "Periscope",
                    link: "#",
                    image: "./src/assets/img/footer-periscope.png"
                },
             
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
            <div>
                <div>
                    <button>
                        sign-up now!
                    </button>
                </div>
                <div>
                    <ul>
                        <li>
                            <h3>follow us</h3>
                        </li>
                        <li  v-for="(element, index) in ArrayContacts" :key="index">
                            <figure>
                                <a :href="element.link">
                                    <img  :src="`${element.image}`" >
                                </a>
                            </figure>
                        </li>
                    </ul>
                </div>
            </div>
        </section>
    </footer>
</template>

<style scoped lang="scss">
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;
    
    section:first-child{
        > div {
            @include GeneralWidth;
            background-image: url("../assets/img/dc-logo-bg.png");
            background-position: right;
            background-repeat: no-repeat;

    
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
    
    section:last-child{
        background-color: rgba(48, 48, 48, 1);
        > div{
            @include GeneralWidth;
            @include PositionFlex;
            div:first-child{
                button{
                    background-color: rgba(48, 48, 48, 1);
                    border: 2px solid $ColorBlue;
                    padding: 10px;
                    color: white;
                    text-transform: $textUppercase;
                }
            }

            div:last-child{
                padding: 30px 0;
                ul{
                    @include PositionFlex;
                    gap: 20px;
                    li:first-child{
                        > h3{
                            text-transform: $textUppercase;
                            color: $ColorBlue;
                        }
                    }
                }
            }
        }
    }
</style>


