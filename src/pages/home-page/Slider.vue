<template>
    <div class="slider" ref="slider">
        <div class="slider__line" ref="line">
            <div class="slider__item" v-for="slider in sliders" :key="slider" ref="item" :style="`background: url(${slider.imgPath})`">
                <div class="container">
                    <div class="slider__container">
                        <div class="slider__text-container">
                            <h2 class="slider__title"> {{ slider.title }} </h2>
                            <p class="slider__text"> {{ slider.text }} </p>
                        </div>
                        <div class="slider__button-container">
                            <button class="slider__button one" @click="sliderMove(1)"></button>
                            <button class="slider__button two" @click="sliderMove(2)"></button>
                            <button class="slider__button three" @click="sliderMove(3)"></button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { ref, onMounted } from 'vue'

export default {
    data: () => ({
        activeSlide: 1,

        sliders: [
            {
                imgPath: '/img/slider-img-1.2f6fefa1.png', 
                title: 'Книги наше всё!', 
                text: `А также акционеры крупнейших компаний освещают чрезвычайно интересные особенности картины 
                       в целом, однако конкретные выводы, разумеется, своевременно верифицированы!`
            },
            {
                imgPath: '/img/slider-img-2.44763aad.png', 
                title: 'Красивая библиотека!', 
                text: `А также акционеры крупнейших компаний освещают чрезвычайно интересные особенности картины 
                       в целом, однако конкретные выводы, разумеется, своевременно верифицированы!`
            },
            {
                imgPath: '/img/slider-img-3.bd7281ff.png', 
                title: 'Молодые авторы!', 
                text: `А также акционеры крупнейших компаний освещают чрезвычайно интересные особенности картины 
                       в целом, однако конкретные выводы, разумеется, своевременно верифицированы!`
            }
        ],
    }),

    methods: {
        returnWidth () {
            return this.$refs.slider.clientWidth;
        },

        returnHeight () {
            return this.$refs.slider.clientHeight;
        },

        normalizeWidthItemBlocks () {
            const item = this.$refs.item;

            let sliderLine = this.$refs.line;

            item.forEach(element => {
                element.style.width  = `${this.returnWidth()}px`;
                element.style.height = `${this.returnHeight()}px`;

                sliderLine.style.width = `${this.returnWidth() * item.length}px`;
            });
        },

        sliderMove (number) {
            let sliderLine = this.$refs.line;

            if (number === 1) {
                sliderLine.style.transform = `translateX(${-this.returnWidth() * 0}px)`;
            }

            if (number === 2) {
                sliderLine.style.transform = `translateX(${-this.returnWidth() * 1}px)`;
            }

            if (number === 3) {
                sliderLine.style.transform = `translateX(${-this.returnWidth() * 2}px)`;
            }
        }
    },

    mounted () {
        this.normalizeWidthItemBlocks();
    },
}

</script>

<style lang="scss">

@import '../../assets/styles/variable.scss';

.slider {

    overflow: hidden;
    width: 100%;
    height: 750px;
    margin-top: 50px;

    @media(max-width:1920px){
        max-width: 1900px;
        width: 100%;
    }

    &__img {
        width: 100%;
        height: 750px;
        position: absolute;
        z-index: -1;
    }

    &__item {  
        height: 750px;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    &__container {
        height: 500px;
        width: 100%;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
    }

    &__line {
        display: flex;
        justify-content: space-between;
        transition: 300ms;
    }

    &__text {
        font-family: Comfortaa-Regular;
        font-size: 30px;
        line-height: 33px;

        color: #FFFFFF;

        @include media ($xs) {
            font-size: 20px;
        }

        @include media ($xs) {
            font-size: 20px;
            line-height: 25px;
        }

        &-container {
            max-width: 1000px;
            height: 282px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }
    }

    &__title {
        font-family: Comfortaa-Bold;
        font-style: normal;
        font-weight: bold;
        font-size: 72px;
        line-height: 75px;
        color: #fff;

        @include media ($xs) {
            font-size: 50px;
            line-height: 50px;
        }
    }

    &__button {
        width: 50px;
        height: 50px;
        background: #fff;
        border-radius: 100%;
        border: none;
        outline: none;
        cursor: pointer;
        transition: background 500ms;
        margin: 0 5px;

        @include media ($xs) {
            width: 30px;
            height: 30px;
            margin-top: 5px;
        }

        &:hover {
            background: #7A94A3;
        }

        &-container {
            top: 860px;
            left: 800px;
            width: 100%;
            display: flex;
            justify-content: center;
        }

    }

}

</style>