<template>
    <div class="container">
        <quote-grid :quotes="quotes"></quote-grid>
    </div>
</template>

<script>
import quoteGrid from './components/QuoteGrid.vue';

export default {
    data: function() {
        return {
            quotes: ['The default quote'],
            maxQuotes: 10,
        };
    },
    components: {
        quoteGrid,
    },
};
</script>

<style>
</style>
