<template>
    <div class="buybook">
        <div class="container">
        <div class="buybook__container">
            <div class="buybook__title">
            <router-link to="" class="buybook__title-text">Купить книгу</router-link>
            <span class="buybook__title-icon"><i class="fal fa-chevron-right"></i></span>
        </div>
            <div class="buybook__content">
                <div class="buybook__content-cover">
                    <img src="../../assets/img/crime.png" alt="" class="buybook__content-cover-img">
                </div>
                <div class="buybook__content-info">
                    <h2 class="buybook__content-info-title">Преступление и наказание</h2>
                    <h3 class="buybook__content-info-author">Федор Достоевский</h3>
                    <h3 class="buybook__content-info-plot">Кратко о сюжете:</h3>
                    <p class="buybook__content-info-plot-text">Нищий студент совершает убийство богатой старухи ради наживы. После добровольного признания герой отбывает наказание на каторге, где происходи его духовное перерождение.</p>
                    <div class="buybook__content-info-btn">
                        <router-link to="" class="buybook__content-info-btn-b">Купить</router-link>
                    </div>
                </div>
            </div>
        </div>
    </div>
    </div>
</template>

<style lang="scss">

@import '../../assets/styles/variable.scss';

.buybook{
    &__title {
        font-family: Comfortaa-Light;
        font-style: normal;
        display: flex;
        margin-bottom: 95px;
        
        @include media ($xs) {
            justify-content: center;
            margin-bottom: 15px;
        }
        
        &-text {
            color: #000000;
            margin-right: 10px;
            font-size: 48px;
            
            @include media ($xs) {
                font-size: 30px;
            }
        }
        
        &-icon {
            padding-top: 5px;
            font-size: 30px;
        }
    }
    
    &__content {
        display: flex;
        margin-bottom: 150px;
        
        @include media ($md) {
            flex-wrap: wrap;
            margin-bottom: 50px;
        }
        
        &-cover {
            &-img{
                height: 600px;
                
                @include media ($mini) {
                    margin: 0;
                    width: 320px;
                }  
            }
        }
        
        &-info {
            display: flex;
            flex-direction: column;
            
            &-title {
                font-family: Comfortaa-Regular;
                font-size: 30px;
                margin-left: 40px;
                padding-top: 40px;
                margin-bottom: 64px;
                color: #000000;
                
                @include media ($md) {
                    margin: 10px 0;
                    align-items: center;
                    padding: 0;
                }
            }
            
            &-author {
                font-family: Comfortaa-Light;
                font-size: 30px;
                line-height: 40px;
                margin-left: 40px;
                margin-bottom: 15px;
                color: #000000;
                
                @include media ($md) {
                    margin: 10px 0;
                }
            }
            
            &-plot {
                font-family: Comfortaa-Light;
                font-size: 30px;
                line-height: 40px;
                margin-left: 40px;
                margin-bottom: 39px;
                color: #000000;
                
                @include media ($md) {
                    margin: 10px 0;
                }
                
                &-text {
                    font-family: Comfortaa-Bold;
                    font-size: 25px;
                    line-height: 40px;
                    color: rgba(0, 0, 0, 0.35);
                    margin-left: 40px;
                    text-align: justify;
                    @include media ($md) {
                        margin: 0px;
                        width: 100%;
                        font-size: 20px;
                        line-height: 30px;
                        margin-bottom: 10px;
                    }
                    
                }
            }
            
            &-btn {
                width: 100%;
                height: 100%;
                display: flex;
                align-items: center;
                justify-content: center;
                
                
                &-b {
                    font-family: Comfortaa-Bold;
                    font-size: 30px;
                    line-height: 54px;
                    color: #FFFFFF;
                    background: rgba(155, 195, 255, 0.85);
                    border-radius: 49px;
                    padding: 15px 50px;
                    
                    @include media ($md) {
                        margin-bottom: 15px;
                        
                    }
                }
            }
        }
    }
}



</style>
