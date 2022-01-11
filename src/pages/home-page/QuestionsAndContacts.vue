<template>
    <div class="questions">
        <div class="container">
            <div class="questions__container">
                <div class="questions__title">
                    <router-link to="" class="questions__title-text">Вопросы и контакты</router-link>
                    <span class="questions__title-icon"><i class="fal fa-chevron-right"></i></span>
                </div>
                <div class="questions__content">
                    <div class="questions__content-q">
                        <h2 class="questions__content-q-title">Часто задaваемые вопросы:</h2>
                    <ul class="questions__content-q-list">
                        <li class="questions__content-q-list-l" v-for="question in questions" :key="question">
                            <router-link to="" class="questions__content-q-list-l-link">{{ question }}</router-link>
                        </li>
                    </ul>
                    </div>
                    <div class="questions__content-c">
                            <h3 class="questions__content-c-num">Телефон: (998) 99 923 65 12</h3>
                        <div class="questions__content-c-adress">
                            <h3 class="questions__content-c-adress-title">Адрес:</h3>
                            <h3 class="questions__content-c-adress-text">Город Ташкент, улица Чилонзар 16, дом 23 </h3>
                        </div>
                        <div class="questions__content-c-filials">
                            <h3 class="questions__content-c-filials-text">Филиалы: Чилонзар, Сергили, Якосарай , Юнусабад</h3>
                        </div>
                    </div>
                </div>    
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data: () => ({
        questions: ['Почему именно у нас?','Зачем читать книгу?','Есть ли у нас акции?','Об авторском праве','Где купить книгу?','Где находитесь?','Качество книг']
    })
}
</script>

<style lang="scss">

@import '../../assets/styles/variable.scss';

.questions {
    &__title {
        font-family: Comfortaa-Light;
        font-style: normal;
        display: flex;
        margin-bottom: 80px;
        
        @include media ($xs) {
            justify-content: center;
            margin-bottom: 15px;
        }
        
        &-text {
            color: #000000;
            margin-right: 10px;
            font-size: 48px;
            
            @include media ($xs) {
                font-size: 25px;
            }
        }
        
        &-icon {
            padding-top: 5px;
            font-size: 30px;
        }
    }
    &__content {
        display: flex;
        justify-content: space-between;
        margin-bottom: 100px;
        font-family: Comfortaa-Bold;
        font-size: 30px;
        
        @include media ($md) {
            flex-wrap: wrap;
            font-size: 20px;
        }
        @include media ($md) {
                            
                        }
        
        &-q {
            &-title {
                font-size: 30px;
                font-style: normal;
                line-height: 40px;
                color: #000000;
                margin-bottom: 15px;
            }
            &-list {
                &-l {
                    &-link {
                        font-style: normal;
                        line-height: 40px;
                        color: #B7B7B7;
                        
                        
                    }
                }
                
                @include media ($md) {
                    margin-bottom: 20px;
                }
            }
        }
        &-c {
            max-width: 587px;
            width: 100%;
            line-height: 40px;
            
            &-num {
                margin-bottom: 20px;
            }
            
            &-adress {
                margin-bottom: 20px;
                line-height: 50px;
            }
            
            &-filials {
                line-height: 50px;
            }
        }
    }
}


</style>
