<template lang="html">
  <div class="row">
      <singleQuote v-for="quote in quotes" @click.native="deleteQuote(index)">{{ quote }}</singleQuote>
  </div>
</template>

<script>
import singleQuote from './SingleQuote.vue';

export default {
    props: ['quotes'],
    components: {
        singleQuote,
    },
    methods: {
        deleteQuote(index) {
            this.$emit('quoteDeleted', index);
        },
    },
};
</script>

<style lang="css">
</style>
