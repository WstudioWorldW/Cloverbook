<template>
    <div class="manga">
        <div class="container__big">
            <h2 class="title">
                <router-link to="" class="title__link"> Манга </router-link>
                <span class="icons__title"><i class="fal fa-chevron-right icon__title"></i></span>
            </h2>
            <div class="container">
                <div class="block__container">
                    <div class="block__container-item" v-for="manga in mangas" :key="manga">
                        <img :src="manga.imgPath" alt="manga" class="block__img">
                        <router-link to="" class="block__text"> {{ manga.title }} </router-link>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

export default {
    data: () => ({
        mangas: [
            {imgPath: require('@/assets/img/manga/m1.png'), title: 'Bunny Senpai'},
            {imgPath: require('@/assets/img/manga/m2.png'), title: 'Токиский гуль'},
            {imgPath: require('@/assets/img/manga/m3.png'), title: 'Пять невест'},
            {imgPath: require('@/assets/img/manga/m4.png'), title: 'Demon Slayer'},
        ]
    })
}

</script>