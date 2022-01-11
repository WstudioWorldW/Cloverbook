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

// .header имеет высоту 100vh, 
// при дальнейшей верстки следует отключить это сойство

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

</style>