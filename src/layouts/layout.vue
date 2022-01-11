<template>

    <Header />

    <main class="main">

        <Home />

    </main>

    <Footer />

</template>

<script>

import Header from '../components/Header.vue';
import Footer from '../components/Footer.vue';
import Home from '../views/Home.vue';

export default {
    components: {
        Header, Footer, Home
    }
}

</script>