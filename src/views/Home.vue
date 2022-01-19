<template>
    <Slider />
    <Bestsellers />
    <Manga />
    <Beginners />
    <Buybook />
    <Questions />
</template>

<script>

import Slider from '@/pages/home-page/Slider.vue';
import Questions from '@/pages/home-page/QuestionsAndContacts.vue';
import Buybook from '@/pages/home-page/Buybook.vue';
import Bestsellers from '@/pages/home-page/BestSellers.vue';
import Manga from '@/pages/home-page/Manga.vue';
import Beginners from '@/pages/home-page/Beginners.vue';

export default {
    components: {
      Slider, Buybook, Questions, 
      Bestsellers, Manga, Beginners
    }
}

</script>

<style lang="scss">

</style>
