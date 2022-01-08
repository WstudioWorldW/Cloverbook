<template>
    <header class="header">
        <div class="container">
            <div class="header__container">
                <div class="header__logo-container">
                    <div class="header__logo">
                        <img src="../assets/img/Logo.png" alt="logo" class="logo">
                        <p class="header__logo-title">Clovebook</p>
                    </div>
                    <div class="header__icons">
                        <ul class="header__icons-ul">
                            <li v-for="icon in icons" :key="icon">
                                <router-link to="" class="icons"><i :class="icon"></i></router-link>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
            <nav class="nav">
                <div class="nav__container">
                    <ul class="nav__ul">
                        <li class="nav__link" v-for="category in categories" :key="category">
                            <router-link to="" class="nav__link">{{ category }}</router-link>
                        </li>
                    </ul>
                </div>
            </nav>
        </div>
    </header>

    <main class="main">

    </main>

    <footer class="footer">
        <div class="container">
            <div class="footer__container">
                <div class="footer__text">
                    <p class="footer__text-title">Cайт разработон компанией</p>
                    <div class="footer__container-logo-mini">
                        <img src="../assets/img/Logo-white.png" alt="" class="logo__footer-mini">
                        <p class="footer__logo-text-mini">Clovebook</p>
                    </div>
                </div>
                <div class="footer__container-logo">
                    <img src="../assets/img/Logo-white.png" alt="logo-white" class="logo__footer">
                    <p class="footer__logo-text">Clovebook</p>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>

export default {
    data: () => ({
        icons: ['far fa-heart','far fa-shopping-cart','far fa-user user','far fa-phone-alt'],
        categories: ['Главная','О нас','Книги','Жанры','Авторы','Издатели']
    }) 
}

</script>

<style lang="scss">

@import '../assets/styles/variable.scss';

.header {
    
    margin-top: 30px;
    height: 100vh;

    @include media ($lg) {
        margin-top: 20px;
    }  

    &__logo {
        display: flex;
        align-items: flex-end;

        &-title {
            font-family: Comfortaa-Bold;
            font-style: normal;
            font-size: 30px;
            line-height: 33px;

            color: #000000;

            @include media ($lg) {
                font-size: 20px;
            }   

            @include media ($xs) {
                font-size: 16px;
                line-height: 16px;
            }  

        }

        &-container {
            width: 100%;
            display: flex;
            justify-content: space-between;
        }

    }

    &__icons {
        max-width: 160px;
        width: 100%;
        display: flex;
        align-items: flex-end;

        @include media ($xs) {
            width: 100px;
        }  

        &-ul {
            width: 100%;
            display: flex;
            justify-content: space-between;
        }

    }

    &__container {
        max-width: 1140px;
        width: 100%;
        margin: 0 auto;
    }

}

.logo {
    border: 2px solid #000;
    border-radius: 100%;
    padding: 5px;

    @include media ($xs) {
        width: 50px;
        height: 50px;
    }  

    &__footer {
        border: 2px solid #fff;
        border-radius: 100%;
        padding: 5px;

        @include media ($md) {
            width: 40px;
            height: 40px;
        } 

        &-mini {
            width: 30px;
            height: 30px;
            border: 2px solid #fff;
            border-radius: 100%;
            padding: 2px;
            margin: 0  0 0 10px;
        }

    }

}

.nav {
    margin-top: 30px;
    width: 100%;

    &__container {
        width: 100%;
    }

    &__ul {
        width: 100%;
        display: flex;
        justify-content: space-between;

        @include media ($md) {
            flex-wrap: wrap;
        } 

        @include media ($xs) {
            justify-content: start;
        } 

    }

    &__link {
        font-family: Comfortaa-Bold;
        font-style: normal;
        font-size: 36px;
        line-height: 40px;

        color: #000000;

        transition: color 500ms;

        &:hover {
            color: red;
        }

        @include media ($lg) {
            font-size: 30px;
        }

        @include media ($md) {
            font-size: 20px;
            margin: 0 10px 0 0;
        }  

        @include media ($xs) {
            font-size: 16px;
            line-height: 25px;
        }  

        @include media ($xs) {
            font-size: 14px;
        }  

    }

}

.footer {

    background: #000;
    color: #fff;
    height: 130px;

    @include media ($xs) {
        height: 80px;
    }

    .footer__container {
        height: 130px;
        display: flex;
        justify-content: space-between;
        align-items: center;

        @include media ($xs) {
            justify-content: center;
        }

        @include media ($xs) {
        height: 80px;
    }

        &-logo {
            display: flex;
            align-items: flex-end;

            @include media ($xs) {
                display: none;
            }

            &-mini {    
                display: flex;
                align-items: flex-end;
            }

        }

    }

    &__logo {
        

        &-text {
            width: 173px;
            height: 23px;

            font-family: Comfortaa-Bold;
            font-style: normal;
            font-size: 30px;
            line-height: 33px;

            color: #FFFFFF;

            @include media ($lg) {
                font-size: 16px;
            }   

            @include media ($xs) {
                font-size: 14px;
                line-height: 14px;
            }  

            &-mini {
                font-family: Comfortaa-Bold;
                font-style: normal;
                font-weight: bold;
                font-size: 18px;
                line-height: 20px;

                color: #FFFFFF;

                @include media ($md) {
                    font-size: 10px;
                }

                @include media ($md) {
                    font-size: 8px;
                }
            
            }

        }

    }

    &__text {

        display: flex;

        &-title {
            font-family: Comfortaa-Bold;
            font-style: normal;
            font-weight: bold;
            font-size: 30px;
            line-height: 33px;

            color: #FFFFFF;

            @include media ($lg) {
                font-size: 20px;
            }

            @include media ($md) {
                font-size: 16px;
                margin: 0 10px 0 0;
            }  

            @include media ($xs) {
                font-size: 14px;
            }  

        }

    }

}

</style>