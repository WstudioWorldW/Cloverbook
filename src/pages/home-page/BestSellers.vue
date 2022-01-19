<template>
    <div class="bestsellers">
        <div class="container__big">
            <h2 class="title">
                <router-link to="" class="title__link"> Бестселлеры </router-link>
                <span class="icons__title"><i class="fal fa-chevron-right icon__title"></i></span>
            </h2>
            <div class="container">
                <div class="block__container">
                    <div class="block__container-item" v-for="bestseller in bestsellers" :key="bestseller">
                        <img :src="bestseller.imgPath" alt="bestseller" class="block__img">
                        <router-link to="" class="block__text"> {{ bestseller.title }} </router-link>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

export default {
    data: () => ({
        bestsellers: [
            {imgPath: require('@/assets/img/bestsellers/b1.png'), title: 'Новый ковчег'},
            {imgPath: require('@/assets/img/bestsellers/b2.png'), title: 'Волчья Луна'},
            {imgPath: require('@/assets/img/bestsellers/b3.png'), title: 'НенавистьЛюбовь'},
            {imgPath: require('@/assets/img/bestsellers/b4.png'), title: 'Metro Exodus'},
        ]
    })
}

</script>