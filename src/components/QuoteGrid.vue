<template lang="html">
  <div class="row">
      <singleQuote v-for="quote in quotes" @click.native="deleteQuote">{{ quote }}</singleQuote>
  </div>
</template>

<script>
import singleQuote from './SingleQuote.vue';

export default {
    props: ['quotes'],
    components: {
        singleQuote,
    },
};
</script>

<style lang="css">
</style>
