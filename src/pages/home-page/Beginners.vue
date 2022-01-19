<template>
    <div class="beginners">
        <div class="container__big">
            <h2 class="title">
                <router-link to="" class="title__link"> Начинающие Авторы </router-link>
                <span class="icons__title"><i class="fal fa-chevron-right icon__title"></i></span>
            </h2>
            <div class="container">
                <div class="block__container">
                    <div class="block__container-item" v-for="beginner in beginners" :key="beginner">
                        <img :src="beginner.imgPath" alt="beginner" class="block__img">
                        <router-link to="" class="block__text"> {{ beginner.title }} </router-link>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

export default {
    data: () => ({
        beginners: [
            {imgPath: require('@/assets/img/beginners/b1.png'), title: 'Квант'},
            {imgPath: require('@/assets/img/beginners/b2.png'), title: 'Пляс Хаоса'},
            {imgPath: require('@/assets/img/beginners/b3.png'), title: 'Я хочу к тебе'},
            {imgPath: require('@/assets/img/beginners/b4.png'), title: 'О Живых и Мёртвых'},
        ]
    })
}

</script>