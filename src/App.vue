<template>
    <div class="container">
        <new-quote @quoteAdded="newQuote"></new-quote>
        <quote-grid :quotes="quotes"></quote-grid>
    </div>
</template>

<script>
import quoteGrid from './components/QuoteGrid.vue';
import newQuote from './components/NewQuote.vue';

export default {
    data: function() {
        return {
            quotes: ['The default quote'],
            maxQuotes: 10,
        };
    },
    methods: {
        newQuote(quote) {
            console.log(this.quotes);
            this.quotes.push(quote);
        },
    },
    components: {
        quoteGrid,
        newQuote,
    },
};
</script>

<style>
</style>
