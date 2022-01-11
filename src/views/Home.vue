<template>
  <buyBook />
  <QuestionsAndContacts />
</template>

<script>
import buyBook from '../pages/home-page/buybook.vue';
import QuestionsAndContacts from '../pages/home-page/QuestionsAndContacts.vue';

export default {
  components: {
    buyBook, QuestionsAndContacts
  }
}

</script>

<style lang="scss">

// .header имеет высоту 100vh, 
// при дальнейшей верстки следует отключить это сойство

</style>
