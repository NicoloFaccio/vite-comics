<script>
  export default{
    name: "AppHeader"
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
               <li>
                   <a href="#">characters</a>
                </li>

               <li>
                   <a href="#">comics</a>
                </li>

               <li>
                   <a href="#">movies</a>
                </li>

               <li>
                   <a href="#">tv</a>
                </li>

               <li>
                   <a href="#">games</a>
                </li>

               <li>
                   <a href="#">collectibles</a>
                </li>

               <li>
                   <a href="#">videos</a>
                </li>

               <li>
                   <a href="#">fans</a>
                </li>

               <li>
                   <a href="#">news</a>
                </li>

               <li>
                   <a href="#">shop</a>
                </li>
            </ul>
            </nav>
            
        </div>
    </header>
</template>

<style>
    header{
        > div {
            display: flex;
            justify-content: space-between;
            align-items: center;

            margin: 0 auto;
            width: 70%;

            text-transform: uppercase;
            
            nav {
                ul {
                list-style-type: none;

                display: flex;
                gap: 15px;

                li {
                    &:hover{ 
                        border-bottom: 1px solid rgba(2, 130, 249, 1);
                    }

                    a {
                        text-decoration: none;
                        color: rgba(104, 92, 86, 1);
                        &:hover{ 
                            color: rgba(2, 130, 249, 1);
                        }
                    }
                }
            }
            }
        }
    }
</style>


