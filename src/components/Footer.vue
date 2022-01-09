<template>

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

<style lang="scss">

@import '../assets/styles/variable.scss';

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